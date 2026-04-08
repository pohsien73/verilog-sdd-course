# Quiz 01

## Multiple choice

1. What is the main goal of SDD in RTL work?
   - A. write RTL faster
   - B. make the specification the source of truth
   - C. remove the need for simulation
   - D. reduce waveform size

2. Which of the following is a bad requirement?
   - A. output shall update on rising edge of clk
   - B. reset is active-low asynchronous
   - C. module should behave properly when busy
   - D. count saturates at 8'hFF

## Short answer

3. Why is a vague requirement dangerous in digital IC design?
4. Name two items that must appear in a good hardware spec.

## Answer key

1. B
2. C
3. Because ambiguity creates mismatched implementation and missed corner cases.
4. Example answers: interface definition, timing behavior, reset behavior, legal/illegal inputs, corner cases.
