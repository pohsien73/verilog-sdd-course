# Lesson 07 - Assertions and Coverage

## Learning goals

- connect design intent to assertions
- understand coverage as feedback for missing tests
- use assertions to stabilize refactoring

## Assertions as executable intent

A written rule in the spec should often become:
- a testcase
- an assertion
- or both

Example intent:
> If FIFO is full and write occurs without read, occupancy shall not increase.

That can become a test and an assertion.

## Coverage mindset

Coverage is not just a number to maximize. It tells you:

- what parts of the design were never exercised
- what scenarios your tests forgot
- whether your spec and test plan are mismatched

## Balanced view

- high coverage with weak checks is dangerous
- strong checks with blind spots are also dangerous

You need both breadth and correctness.
