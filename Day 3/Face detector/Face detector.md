
<img width="512" height="266" alt="image" src="https://github.com/user-attachments/assets/4c81fd6e-b35d-4399-96a6-d4b508ed26df" />
<img width="1575" height="816" alt="image" src="https://github.com/user-attachments/assets/64d8d3f2-ef2a-4b9a-8c0e-cb09598c308a" />
<img width="1571" height="813" alt="image" src="https://github.com/user-attachments/assets/55e80097-eee3-45de-9fe3-809dc76fb737" />
<img width="713" height="365" alt="image" src="https://github.com/user-attachments/assets/40ce5051-3520-484a-a74b-1e09ee1a93da" />

## Project Overview
This project shows a digital hardware design idea. It is about transferring data, between a fast data producer and a slow data consumer without losing any data. To solve this problem a First-In-First-Out memory buffer, also known as a FIFO is used. The FIFO holds the data until the slower consumer is ready to process it.

System. File Structure

face_mod.v (Fast Producer): This module generates and sends 8-bit data continuously at every positive clock edge. It acts as the high-speed source.
fifo.v (Buffer Memory): This is an area-optimized memory buffer. It uses. Write pointers to store data from the producer and feed it to the consumer when needed.
mod_out.v (Slow Consumer): This module uses a 3-state Finite State Machine with states IDLE, READ_PROC. Done. It carefully reads data from the FIFO simulates a processing delay and outputs the result.
top_module.v (Top-Level Wrapper): This is the file that connects the above three modules and wires them together with a global reset signal.
top_module_tb.v (Testbench): This simulation file injects a burst of data to verify that the FIFO successfully buffers it and outputs it sequentially without dropping any initial values.
Simulation of: top_module_tb.v

