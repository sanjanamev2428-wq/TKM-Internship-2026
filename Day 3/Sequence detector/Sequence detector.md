# Sequence detector

## Output Waveform

<img width="1348" height="681" alt="image" src="https://github.com/user-attachments/assets/7d1081a3-0bf3-480f-a49b-8890a6182d11" />

​This waveform illustrates a Sequence Detector in action.
​The system tracks incoming bits on din synchronous to the clock. When a specific target sequence concludes (right around the 105 ns mark where din drops from 1 to 0), the internal state machine satisfies its conditions and sets detected = 1 for a single clock cycle to signal a successful match. Given that it triggers immediately after a long string of 1s ends with a 0, it is highly likely looking for a sequence ending in ...110 or a specific count of consecutive ones followed by a zero.

## Result
The Sequence detector was successfully implemented and simulated.
