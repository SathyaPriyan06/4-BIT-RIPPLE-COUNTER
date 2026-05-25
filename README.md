# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module exper5(input clk, reset, output reg [3:0] q);
    always @(posedge clk or posedge reset)
        if (reset) q[0] <= 0; else q[0] <= ~q[0];

    always @(negedge q[0] or posedge reset)
        if (reset) q[1] <= 0; else q[1] <= ~q[1];

    always @(negedge q[1] or posedge reset)
        if (reset) q[2] <= 0; else q[2] <= ~q[2];

    always @(negedge q[2] or posedge reset)
        if (reset) q[3] <= 0; else q[3] <= ~q[3];
endmodule
```

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:S.Sathya Priyan RegisterNumber:212225230255
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1920" height="994" alt="{0D3011BE-3A72-4720-8E7D-EED109BEDA34}" src="https://github.com/user-attachments/assets/249557ef-7f4a-495e-8e09-63da03d12aee" />


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1920" height="907" alt="{6DCE1D64-542B-493F-ACDF-546E1DC5FE24}" src="https://github.com/user-attachments/assets/939df847-37a5-45bb-8d1e-a1af924fdd02" />


**RESULTS**
Thus the 4 Bit Ripple Counter using verilog is implemented and their functionality using their functional tables is validated.
