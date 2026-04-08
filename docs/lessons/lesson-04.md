# Lesson 04 - TDD Workflow for RTL Modules

## Learning goals

- use a red-green-refactor cycle for RTL
- write a failing test before implementation
- implement the minimum logic required to pass

## RTL TDD loop

1. choose one behavior from the spec
2. write a minimal testcase that fails
3. implement the smallest RTL to make it pass
4. rerun tests
5. clean up without changing behavior

## Example workflow: simple counter

### Step 1: failing test
Write a test expecting reset to clear count.

### Step 2: minimum RTL
Implement reset logic only.

### Step 3: next failing test
Write a test expecting increment when enabled.

### Step 4: minimum RTL update
Add increment path.

This creates confidence in small steps instead of gambling on one large implementation.

## Benefits in hardware

- easier waveform debugging
- smaller bug search space
- stronger regression habits
- safer refactoring

## Limits

TDD is best for small to medium blocks and behavior slices. It becomes harder for full-chip integration, but the mindset still helps.
