# Lesson 02 - Writing Good Hardware Specifications

## Learning goals

After this lesson, you should be able to:

- turn vague requirements into measurable hardware requirements
- specify interfaces, timing, reset, and corner cases
- identify missing information before RTL coding begins

## 1. What makes a bad spec

A bad spec sounds like this:

> Build a FIFO. It should store data and indicate full and empty.

Problems:

- What is data width?
- What is depth?
- Sync or async FIFO?
- When does `full` assert?
- What happens on simultaneous read/write?
- What happens during reset?

## 2. What a good spec contains

A practical hardware spec should contain these sections:

### A. Functional purpose
Describe what the block does in one paragraph.

### B. Interface definition
Document every port:
- direction
- width
- meaning
- valid clock domain

### C. Timing and sequencing
Specify:
- which clock edge matters
- synchronous or asynchronous reset
- combinational or registered outputs
- latency expectations

### D. Behavioral rules
Examples:
- if write occurs when full, data is ignored
- if read occurs when empty, underflow flag asserts
- read and write in same cycle updates occupancy accordingly

### E. Corner cases
Examples:
- reset during transaction
- back-to-back enable pulses
- illegal requests
- unknown initial conditions

## 3. Example: counter spec excerpt

**Module:** saturating up counter

- width: 8 bits
- input: `en`, `rst_n`, `clk`
- output: `count[7:0]`, `sat`
- on each rising edge of `clk`, if `en=1` and counter not max, increment by 1
- if counter is `8'hFF`, hold value and assert `sat=1`
- `sat` deasserts after reset
- reset is active-low asynchronous reset

This spec is already much more testable.

## 4. Checklist before coding

Before writing RTL, ask:

- can I write a testbench directly from this spec?
- could another engineer implement the same behavior from this document?
- are illegal cases defined?
- is output timing stated?

## Common mistake

Designers often define functionality but not *observability*. If you cannot observe correct behavior in simulation, the spec is incomplete.
