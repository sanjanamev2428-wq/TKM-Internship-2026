# DECODER 2x4

## Output Waveform

<img width="1359" height="695" alt="image" src="https://github.com/user-attachments/assets/736b6f47-a0f2-44ca-85c5-9ae6303de313" />

The decoder operates as a standard combinational logic circuit controlled by an enable line (\(tb\_en\)):Gated Disable (\(tb\_en = 0\)): All internal AND gates are masked. Regardless of the input on \(tb\_in[1:0]\), the output bus \(tb\_out[3:0]\) is forced to 0000.Active Decoding (\(tb\_en = 1\)): The circuit decodes the 2-bit binary input into its decimal minterm equivalent. Only one output line is "high" at a time (One-Hot behavior).Boolean EquationsThe operation for each output line is defined by the following logic:\(tb\_out[0] = tb\_en \cdot \overline{tb\_in[1]} \cdot \overline{tb\_in[0]}\)\(tb\_out[1] = tb\_en \cdot \overline{tb\_in[1]} \cdot tb\_in[0]\)\(tb\_out[2] = tb\_en \cdot tb\_in[1] \cdot \overline{tb\_in[0]}\)\(tb\_out[3] = tb\_en \cdot tb\_in[1] \cdot tb\_in[0]\)

## Result
The Decoder 2x4 was successfully implemented and stimulated.
