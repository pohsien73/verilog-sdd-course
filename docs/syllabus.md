# Course Syllabus

## Part 1. Foundation

### Lesson 01. Why SDD, TDD, and BDD matter for RTL
- why code-first RTL creates ambiguity
- why bugs in hardware are expensive
- difference between coding, specifying, testing, and validating behavior
- mapping software development methods into hardware design

### Lesson 02. Writing good hardware specifications
- turning vague requirements into engineering specs
- interface specification
- timing behavior
- reset behavior
- legal / illegal inputs
- corner cases and assumptions

### Lesson 03. From spec to test plan
- requirement traceability
- test matrix design
- positive / negative / boundary tests
- coverage thinking before coding

## Part 2. TDD for Verilog

### Lesson 04. TDD workflow for RTL modules
- write failing tests first
- implement minimum RTL
- rerun tests
- refactor safely

### Lesson 05. Refactoring without breaking behavior
- separating style cleanup from functional change
- guarding behavior with assertions and regression
- identifying brittle testbenches

## Part 3. BDD for hardware behavior

### Lesson 06. BDD for digital design
- using Given / When / Then to describe hardware behavior
- converting scenarios into waveform expectations
- making spec language human-readable and testable

### Lesson 07. Assertions and coverage
- linking expected behavior to SVA concepts
- using assertions to preserve intent
- coverage as a learning loop, not a vanity metric

## Part 4. Capstone

### Lesson 08. Capstone project
- choose FIFO, arbiter, or counter controller
- write the spec
- derive tests
- implement RTL
- define BDD scenarios
- present design tradeoffs
