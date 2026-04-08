# Lesson 01 - Why SDD, TDD, and BDD for RTL

## Learning goals

After this lesson, you should be able to:

- explain why traditional code-first RTL often creates hidden bugs
- distinguish specification, implementation, and verification work
- explain SDD, TDD, and BDD in digital design language

## 1. The old habit: code first

A common beginner workflow in Verilog is:

1. receive a vague requirement
2. immediately write RTL
3. simulate a happy-path testcase
4. fix bugs as they appear

This workflow feels fast, but it creates several problems:

- requirements stay ambiguous
- corner cases are discovered too late
- testbenches are incomplete
- refactoring becomes dangerous
- design reviews argue about interpretation instead of facts

## 2. SDD in hardware

**Spec-Driven Development** means the specification becomes the main source of truth.

For RTL, a good spec includes:

- module purpose
- input / output meaning
- clock and reset behavior
- timing assumptions
- legal and illegal sequences
- corner cases
- measurable acceptance criteria

## 3. TDD in hardware

**Test-Driven Development** does not mean writing a huge UVM environment before RTL.
It means:

- define expected behavior first
- write a failing test
- implement the smallest RTL that makes it pass
- repeat

This is especially effective for:

- counters
- FSMs
- small FIFOs
- arbiters
- protocol sub-blocks

## 4. BDD in hardware

**Behavior-Driven Development** adds a human-readable layer.

Example:

- Given FIFO is empty
- When `rd_en` is asserted
- Then `underflow` shall assert and output data shall remain unchanged

BDD is useful because it bridges:

- spec writers
- RTL designers
- verification engineers
- reviewers

## 5. How the three fit together

- **SDD** tells you what the block must do
- **TDD** gives you a disciplined implementation loop
- **BDD** makes the behavior explicit and reviewable

## Common misunderstanding

Many engineers think hardware is too timing-sensitive for TDD or BDD. In reality, hardware benefits more because misunderstandings are expensive.

## Homework preview

You will inspect a simple up-counter requirement and rewrite it into a proper hardware spec.
