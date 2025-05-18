# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

Step1: Define the specifications and initialize the design.

Step2: Declare the name of the entity and architecture by using VHDL source code.

Step3: Write the source code in VERILOG.

Step4: Check the syntax and debug the errors if found, obtain the synthesis report.

Step5: Verify the output by simulating the source code.

Step6: Write all possible combinations of input using the test bench.

**PROGRAM**
```
module ex10d(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Mohamed Mustafa Hussain RegisterNumber:212224240091

*/

**RTL LOGIC FOR SISO Shift Register**

![444867228-b955afc3-6d1f-40dd-834f-01d3565c8761](https://github.com/user-attachments/assets/1d18b23a-a635-45a9-aad5-1a8c70f4a86a)


**TIMING DIGRAMS FOR SISO Shift Register**

![444867234-55e45435-e367-4f54-876d-ce64ea9492c1](https://github.com/user-attachments/assets/7386f277-ea2c-410a-a80f-7212d2e2d708)


**RESULTS**

Thus the OUTPUT of 8-bit shift register is verified by synthesizing and simulating the VERILOG code.
