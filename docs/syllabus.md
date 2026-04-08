# Full Course Syllabus

## Course title
**SDD / TDD / BDD for Verilog and Digital IC Design**

## Course positioning
A practical engineering course for applying structured development methods to RTL design, verification planning, and digital block implementation.

---

## Part 1. Foundation Mindset

### Lesson 01. Why SDD, TDD, and BDD matter for RTL
**What you learn**
- why code-first RTL creates ambiguity and hidden bugs
- difference between implementation, verification, and specification
- how software process ideas map into digital hardware design

**Key deliverable**
- a written reflection on the failure modes of code-first design

### Lesson 02. Writing good hardware specifications
**What you learn**
- how to define module intent
- how to write interface, timing, reset, and edge-case sections
- how to remove ambiguity from engineering language

**Key deliverable**
- a rewritten clean hardware spec for a simple digital block

### Lesson 03. From spec to test plan
**What you learn**
- requirement traceability
- positive / boundary / negative tests
- how to build a verification matrix before RTL exists

**Key deliverable**
- a test matrix for a counter or FIFO

---

## Part 2. Spec-Driven Development for RTL

### Lesson 04. Spec decomposition and requirement quality
**What you learn**
- how to split functional, temporal, and error-handling behavior
- how to detect underspecified requirements
- how to define acceptance criteria

**Key deliverable**
- a requirement review checklist

### Lesson 05. Interface contracts and timing contracts
**What you learn**
- assumptions vs guarantees
- producer / consumer contracts
- synchronous timing and one-cycle / multi-cycle expectations

**Key deliverable**
- a contract sheet for a digital interface

### Lesson 06. Corner cases and failure-oriented thinking
**What you learn**
- why edge cases should be designed before coding
- how to think in terms of overflow, underflow, illegal states, reset races, and sequencing hazards

**Key deliverable**
- a corner-case catalog for a chosen module

---

## Part 3. TDD for Verilog

### Lesson 07. TDD workflow for RTL modules
**What you learn**
- red / green / refactor loop for hardware
- writing the first failing test
- implementing the minimum RTL to pass

**Key deliverable**
- a TDD loop write-up for a counter

### Lesson 08. Writing effective small testbenches
**What you learn**
- how to keep testbenches behavior-focused
- avoiding over-coupling to implementation details
- organizing tests for fast reruns

**Key deliverable**
- a compact testbench for a small block

### Lesson 09. Refactoring without breaking behavior
**What you learn**
- separating cleanup from functional change
- protecting expected behavior with regression
- recognizing brittle tests

**Key deliverable**
- a refactor plan and regression checklist

---

## Part 4. BDD and Communication Quality

### Lesson 10. BDD for hardware behavior
**What you learn**
- using Given / When / Then in digital design
- making behaviors reviewable by humans before simulation
- turning scenarios into directed tests

**Key deliverable**
- 6 BDD scenarios for a digital module

### Lesson 11. Assertions and intent preservation
**What you learn**
- when a rule should become an assertion
- assertion ideas from spec statements
- using assertions as guardrails during change

**Key deliverable**
- 5 assertion candidates from a spec

### Lesson 12. Coverage and requirement completeness
**What you learn**
- coverage as a learning feedback loop
- linking tests to requirements
- finding untested behaviors systematically

**Key deliverable**
- a requirement coverage review

---

## Part 5. Capstone Project

### Lesson 13. Capstone architecture and planning
Choose one project:
- synchronous FIFO
- round-robin arbiter
- programmable counter controller
- packet-valid handshake controller

### Lesson 14. Capstone implementation and review
**Final deliverables**
- specification
- interface contract
- test plan matrix
- RTL implementation
- BDD scenario set
- assertion list
- engineering reflection report

---

## Assessment model

### Quiz checkpoints
- Quiz 01: foundation and spec quality
- Quiz 02: TDD and test planning
- Quiz 03: BDD, assertions, and coverage
- Quiz 04: capstone readiness

### Homework checkpoints
- HW 01: rewrite a weak requirement into a proper spec
- HW 02: derive a test plan from a hardware spec
- HW 03: write BDD scenarios for an arbiter
- HW 04: define assertions from a FIFO spec
- HW 05: perform a mini capstone review

---

## Suggested pacing

### 5-week intensive version
- Week 1: Lesson 01-03
- Week 2: Lesson 04-06
- Week 3: Lesson 07-09
- Week 4: Lesson 10-12
- Week 5: Lesson 13-14 + capstone

### 10-week part-time version
- one to two lessons per week with homework

---

## Final result
By the end of the course, the student should be able to run a small but professional-grade RTL workflow driven by specification clarity and verification discipline.
