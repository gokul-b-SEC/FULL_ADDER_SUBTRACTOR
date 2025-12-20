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

FULL ADDER

<img width="382" height="350" alt="image" src="https://github.com/user-attachments/assets/7697b89a-e7a5-4bd9-abf5-f72f7c73f549" />

FULL SUBRACTOR

<img width="376" height="350" alt="image" src="https://github.com/user-attachments/assets/2bf08f94-dc71-476d-8728-983b1b9e6a84" />


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:GOKUL B
RegisterNumber: 25008644
*/
```

```
FULL ADDER

module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
```
FULL SUBTRACTOR

module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule
```
**RTL Schematic**
FULL ADDER

<img width="725" height="426" alt="image" src="https://github.com/user-attachments/assets/26b61193-b879-4b92-bacb-3a95786323c5" />

FULL SUBRACTOR

<img width="729" height="267" alt="image" src="https://github.com/user-attachments/assets/7d75e18d-e63b-4093-b8a0-f96e59842365" />

**Output Timing Waveform**
FULL ADDER

<img width="773" height="287" alt="image" src="https://github.com/user-attachments/assets/29cc19c9-9041-409e-b982-c3e3af645d1c" />

FULL SUBRACTOR

<img width="773" height="268" alt="image" src="https://github.com/user-attachments/assets/f1f63343-9958-495a-a1c0-c155bb92e094" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



