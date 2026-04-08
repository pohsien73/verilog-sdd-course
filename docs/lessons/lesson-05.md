# Lesson 05 - Refactoring Without Breaking Behavior

## Learning goals

- separate functional change from cleanup
- protect design intent with regression tests
- identify fragile testbenches

## What is refactoring in RTL?

Refactoring means changing structure without changing behavior.

Examples:
- renaming signals
- splitting logic into clearer blocks
- simplifying FSM encoding style
- replacing duplicated combinational logic with helper expressions

## Safe refactoring rules

- change one thing at a time
- rerun full regression after each change set
- avoid changing spec and implementation at once
- preserve test names and acceptance criteria

## Fragile testbench warning signs

- tests depend on internal signals too much
- tests assume exact implementation ordering not required by spec
- tests break after harmless naming changes

A good testbench checks contractual behavior, not private implementation details.
