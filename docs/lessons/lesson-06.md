# Lesson 06 - BDD for Digital Design

## Learning goals

- express hardware behavior using Given / When / Then
- use scenario language to clarify ambiguous requirements
- translate scenarios into directed tests

## Example

Given the FIFO is empty  
When `rd_en` is asserted on the rising edge of `clk`  
Then `empty` remains asserted and underflow handling shall occur

This style helps teams discuss behavior before code.

## Why BDD is useful in RTL teams

- less ambiguity in design reviews
- easier communication across RTL and verification teams
- easier transformation into directed tests or assertions

## Good BDD scenario traits

- one behavior per scenario
- explicit initial condition
- explicit trigger
- explicit expected outcome

## Poor BDD scenario example

Given normal operation  
When something weird happens  
Then system should behave properly

This is vague and not testable.
