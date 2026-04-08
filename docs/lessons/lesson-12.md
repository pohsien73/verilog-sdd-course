# Lesson 12 - Coverage and Requirement Completeness

## Learning goals

After this lesson, you should be able to:

- treat coverage as a question generator, not a vanity metric
- find gaps between requirements and tests
- perform a basic requirement completeness review

## 1. The danger of shallow confidence

Many engineers feel safe after a few passing tests. That is false confidence.

Coverage exists to answer:
- what have we not exercised?
- what requirements have no protection?
- what corners were assumed but never tested?

## 2. Requirement coverage review

Create a simple table:

| Requirement | Test exists? | Assertion exists? | Covered? |
|---|---|---|---|

This is powerful even before formal coverage tools.

## 3. Coverage questions worth asking

- Have I tested reset from meaningful states?
- Have I tested boundary transitions?
- Have I tested negative behaviors?
- Have I tested simultaneous events?
- Have I tested legal but unusual sequences?

## 4. What coverage cannot do

Coverage cannot guarantee the checks are correct. You can hit code and still miss intent.

## 5. Better engineering habit

Use coverage review after every test expansion cycle.

Ask:
> What requirement still has no trustworthy protection?

## Summary

Coverage should drive learning, not ego.
