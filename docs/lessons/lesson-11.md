# Lesson 11 - Assertions and Intent Preservation

## Learning goals

After this lesson, you should be able to:

- identify which rules should become assertions
- use assertions to protect intent during evolution
- connect specs, tests, and assertions in one chain

## 1. What assertions are really for

Assertions are not only bug catchers. They are executable statements of design intent.

If the spec says:
> grant shall be one-hot when any valid request exists

that statement is a good assertion candidate.

## 2. When to write an assertion

Write an assertion when:
- a rule must never be violated
- a protocol condition must hold
- a state relationship should remain invariant
- refactoring could silently break a guarantee

## 3. Examples of good assertion targets

- one-hot grant rules
- occupancy never negative
- full and empty not asserted together in impossible states
- reset establishes known outputs
- valid / ready handshakes obey protocol rules

## 4. Assertions vs tests

Tests ask:
- does behavior occur under this scenario?

Assertions ask:
- is this forbidden behavior ever happening at all?

You need both.

## 5. Practical workflow

For each major requirement, ask:
- should this be tested?
- should this be asserted?
- should it be both?

## Summary

Assertions reduce the risk that future edits slowly erode your original intent.
