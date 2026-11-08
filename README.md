# Custom BCD-to-7-Segment Decoder (IC 4511 Equivalent) using Basic Logic Gates

## Project Overview & Objective
- Design and simulate a combinational logic circuit that replicates the exact functional behavior of a standard CMOS IC CD4511 BCD-to-7-Segment Decoder/Driver.
- Convert a 4-bit Binary Coded Decimal (BCD) input (weighted 8, 4, 2, 1) into 7 corresponding active-high segment outputs (A, B, C, D, E, F, G) to drive a 7-segment display layout.

## Hardware / Component Architecture (Logisim v2.7.1)
- **Inputs:** 4 individual binary input pins representing bits [8, 4, 2, 1] with NOT gate buffers to supply both true and complemented input rails.
- **Decoding Logic:** A bank of 10 AND gates (labeled 0 through 9) configured to detect each specific decimal combination from the 4-bit BCD input space.
- **Output Drivers:** A bank of 7 OR gates (labeled A through G) connected to the appropriate minterms from the AND gate array to drive each individual display segment.
- **Outputs:** 7 output indicator pins (A through G).

### Circuit Implementation (Logic Gates)
![Logic Gates Design](docs/Logic%20Gates.png)

## How to Test and Run the Simulation
1. Open the project file in Logisim.
2. Navigate to the "Test" circuit containing the IC CD4511 custom circuit block.
3. Use the **Poke Tool** to toggle the 4 input pins (8, 4, 2, 1) between 0 and 1.
4. Observe the 7 output pins (A to G) change states to verify correct segment activation for each decimal digit 0 through 9.

### Simulation Test Bench
![Logic Test Bench](docs/Logic%20Test.png)
