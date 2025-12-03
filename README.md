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
<img width="549" height="369" alt="Screenshot 2025-12-03 102024" src="https://github.com/user-attachments/assets/e2f70b26-1ac6-4a53-b931-aa5ad2fb64bb" />
<img width="634" height="296" alt="Screenshot 2025-12-03 103716" src="https://github.com/user-attachments/assets/20c8e4a4-4991-49ea-8717-2227a52e003e" />
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
<img width="559" height="223" alt="Screenshot 2025-12-03 102003" src="https://github.com/user-attachments/assets/712b6d0d-0b0c-4dba-ae15-b429441adb6f" />
<img width="595" height="280" alt="Screenshot 2025-12-03 103519" src="https://github.com/user-attachments/assets/f5b26e88-7f9c-4a3a-b399-76be4f44d653" />



**Output Timing Waveform**
<img width="1910" height="333" alt="Screenshot 2025-12-03 102130" src="https://github.com/user-attachments/assets/a97b6864-bb1f-4bce-9152-910f193b0521" />
<img width="1913" height="327" alt="Screenshot 2025-12-03 103640" src="https://github.com/user-attachments/assets/e2fffb59-2142-45ea-8e5a-7d3d291da5c0" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



