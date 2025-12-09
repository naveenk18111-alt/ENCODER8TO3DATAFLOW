# ENCODER 8TO3 DATAFLOW Modelling
## Developed By: NAVEENKUMAR V
## Ref. No: 25016071

## AIM:
To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

## SOFTWARE REQUIRED:
Quartus prime

## THEORY:

### Encoder 8 To 3

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

### Truth Table:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

## Procedure:

1.   Write the Verilog Code:
        * Define the module with 8 inputs (D0–D7) and 3 outputs (A0–A2).
        * Use dataflow modelling (assign statements) to implement the logical expressions.
2.   Create Project in Quartus Prime
        * Open Quartus Prime and start a new project.
        * Add the Verilog source file (encoder_8to3.v) to the project.
3.   Compile the Design
        * Run compilation to check for syntax errors.
        * Verify the RTL schematic generated matches the encoder logic.
4.   Simulate the Encoder
        *  Use the Waveform Editor to apply test inputs one at a time.
        * Observe the outputs (A0–A2) in the timing diagram.

5.   Validate with Truth Table
        * Compare simulation results with the theoretical truth table.
        * Confirm correctness of outputs and document timing diagrams.

## PROGRAM:
```
module encoder_8to3(din, a, b, c);
input [0:7] din;
output a, b, c;
assign a = din[4] | din[5] | din[6] | din[7];
assign b = din[2] | din[3] | din[6] | din[7];
assign c = din[1] | din[3] | din[5] | din[7];
endmodule
```

## RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling:

## TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling:

## RESULT:
Thus The Implementing Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables executed succesfully.
