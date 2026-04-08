# Lesson 10 - BDD for Hardware Behavior

## Learning goals

After this lesson, you should be able to:

- express hardware requirements in Given / When / Then format
- use scenario writing to clarify corner cases early
- convert scenarios into directed tests and review artifacts

## 1. Why BDD helps hardware teams

BDD is valuable in RTL because many bugs begin as communication failures.

People use the same words differently:
- "hold"
- "ignore"
- "stall"
- "drop"
- "priority"
- "same cycle"

BDD forces explicit sequencing.

## 2. Basic structure

### Given
The initial state or context.

### When
The stimulus or event.

### Then
The expected outcome.

## 3. Example: FIFO scenario

Given the FIFO is full  
When `wr_en` is asserted and `rd_en` is low on the rising edge of `clk`  
Then occupancy shall remain unchanged and overflow handling shall occur

This is much clearer than saying:
> writes are ignored when full

## 4. Scenario writing tips

- mention exact state or flag condition
- mention the trigger precisely
- mention the observable outputs or state effects
- avoid vague words like "correctly" or "normally"

## 5. Good uses of BDD in digital design

- design reviews
- pre-RTL alignment
- verification planning
- onboarding junior engineers
- converting corner cases into assertions

## 6. Limits of BDD

BDD is not a replacement for a timing diagram, detailed spec, or simulation. It is a clarity layer.

## Summary

BDD improves engineering communication quality, and better communication means fewer expensive misunderstandings.
