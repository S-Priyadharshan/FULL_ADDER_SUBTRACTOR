# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

Full Adder:
![image](https://github.com/S-Priyadharshan/FULL_ADDER_SUBTRACTOR/assets/145854138/43a2d1c5-40dd-4871-bd3a-2d347f16609b)


Full Subtractor:
![image](https://github.com/S-Priyadharshan/FULL_ADDER_SUBTRACTOR/assets/145854138/595bc2d2-a2a2-4581-ad7f-021bf17a372c)


**Procedure**
**STEP-1**
Open Quartus Prime software.

**STEP-2**
Create a new project and select the target FPGA device.

**STEP-3**
Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

**STEP-4**
Add the HDL file to the project and compile the design.

**STEP-5**
Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Priyadharshan S
RegisterNumber: 212223240127
*/
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```
**RTL Schematic**

![Screenshot 2024-04-02 150109](https://github.com/S-Priyadharshan/FULL_ADDER_SUBTRACTOR/assets/145854138/f421b463-e248-4009-8541-394b274e8b20)

**Output Timing Waveform**
![Screenshot 2024-04-02 145008](https://github.com/S-Priyadharshan/FULL_ADDER_SUBTRACTOR/assets/145854138/9539cecc-5b1d-44e8-8d94-bac81cdedac9)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



