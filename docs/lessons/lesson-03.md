# Lesson 03 - From Specification to Test Plan

## Learning goals

After this lesson, you should be able to:

- derive a test plan from a hardware spec
- create requirement-to-test traceability
- identify positive, negative, and boundary tests

## 1. Why test planning comes before RTL

If you cannot name the tests before coding, you probably do not understand the design yet.

A test plan prevents two common failures:

- missing corner cases
- overconfidence from one or two passing tests

## 2. Requirement traceability table

Example for a saturating counter:

| Requirement ID | Description | Test case |
|---|---|---|
| R1 | reset clears count to 0 | TC01 reset behavior |
| R2 | count increments when enabled | TC02 single increment |
| R3 | count holds when disabled | TC03 hold behavior |
| R4 | count saturates at max | TC04 saturation |
| R5 | sat flag asserts at max | TC05 saturation flag |

This simple table already raises quality.

## 3. Test categories

### Positive tests
The intended normal behavior.

### Boundary tests
Examples:
- 0 to 1
- max-1 to max
- full to overflow attempt

### Negative tests
Examples:
- read when empty
- illegal enable combinations
- reset during active cycle

## 4. Test planning example

For FIFO, you would plan tests such as:

- reset initializes pointers and flags
- single write updates occupancy
- single read from non-empty FIFO returns expected data
- read from empty triggers underflow handling
- write to full triggers overflow handling
- simultaneous read/write maintains occupancy correctly

## 5. A good test plan is implementation-independent

Bad test name:
- test internal pointer value after write

Better test name:
- verify FIFO occupancy and output behavior after write

The second version preserves freedom to refactor implementation.

## Key idea

A strong test plan tests **behavior**, not coding style.
