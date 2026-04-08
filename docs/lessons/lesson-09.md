# Lesson 09 - Refactoring Without Breaking Behavior

## Learning goals

After this lesson, you should be able to:

- distinguish behavioral change from structural cleanup
- define a safe refactoring sequence for RTL
- use regression and assertions as protection layers

## 1. Why refactoring matters in RTL

Many RTL engineers treat the first working version as sacred because they fear breaking behavior. That fear is understandable, but it creates technical debt.

Typical symptoms:
- unreadable nested logic
- duplicated conditions
- poor naming
- mixed combinational and sequential intent
- difficult debug

Refactoring helps readability and maintainability, but only if you can prove behavior is preserved.

## 2. What counts as refactoring

Examples of refactoring:
- renaming state signals for clarity
- separating next-state logic from state registers
- simplifying duplicated expressions
- reorganizing conditional branches for readability
- isolating flag generation from datapath updates

Not refactoring:
- changing latency
- changing protocol timing
- changing reset semantics
- changing priority rules

Those are functional changes.

## 3. Safe refactoring workflow

1. freeze the current expected behavior
2. list the tests that define that behavior
3. add assertions for key invariants if missing
4. refactor one concern at a time
5. rerun regression after each change set
6. review diffs by intent, not by file size

## 4. Refactor checklist

Before refactoring, ask:
- which behaviors are contractually fixed?
- what tests fail if I accidentally change them?
- are my tests too implementation-specific?
- do I need one temporary assertion before cleanup?

## 5. Example

Suppose a small arbiter has working functionality, but the priority logic is duplicated in two places. A safe refactor would:
- keep external behavior fixed
- extract duplicated logic into a cleaner shared expression
- rerun all granted-request tests
- confirm no change in latency or fairness

## 6. Common trap

Engineers sometimes mix cleanup with feature addition in one commit. That makes reviews weak and debugging painful.

Rule:
> One commit for cleanup. Another commit for behavior change.

## Summary

Refactoring is not risky by itself. Refactoring without behavioral protection is risky.
