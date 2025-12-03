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

**Procedure**

Write the detailed procedure here

**Program:**
<img width="549" height="369" alt="Screenshot 2025-12-03 102024" src="https://github.com/user-attachments/assets/a515253c-2bcb-4457-aca5-0e0294fe4c97" />
<img width="634" height="296" alt="Screenshot 2025-12-03 103716" src="https://github.com/user-attachments/assets/ec407699-4b3a-4e46-941b-8fcff89ac767" />
module exp4no1(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
module exp4no2(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule



/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
<img width="559" height="223" alt="Screenshot 2025-12-03 102003" src="https://github.com/user-attachments/assets/eb0dd714-2e10-47ec-98c2-98aa01bb2aea" />
<img width="595" height="280" alt="Screenshot 2025-12-03 103519" src="https://github.com/user-attachments/assets/7446100d-9416-4dd3-981d-38348b75406d" />





**Output Timing Waveform**
<img width="1910" height="333" alt="Screenshot 2025-12-03 102130" src="https://github.com/user-attachments/assets/c1df97a7-1412-406d-888f-f254309bceb0" />
<img width="1913" height="327" alt="Screenshot 2025-12-03 103640" src="https://github.com/user-attachments/assets/ad326bc6-be84-466d-a36d-05ecd6819c2e" />



**Result:**


Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



