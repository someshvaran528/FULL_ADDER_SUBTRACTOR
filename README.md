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
<img width="393" height="255" alt="image" src="https://github.com/user-attachments/assets/9db6783c-14ec-4d15-8af9-7ecf48f5aab6" />
<img width="257" height="145" alt="image" src="https://github.com/user-attachments/assets/9852f5ae-0914-4ecf-91d8-a107c79c027f" />

**Procedure**

Write the detailed procedure here

**Program:**i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**<img width="874" height="489" alt="Screenshot 2025-10-07 101429" src="https://github.com/user-attachments/assets/8e74944e-4f6d-4817-95f8-81d8065004df" />
<img width="782" height="248" alt="Screenshot 2025-10-07 102914" src="https://github.com/user-attachments/assets/f5bc975a-c004-430f-9d57-257a684299a8" />



**Output Timing Waveform**<img width="1900" height="941" alt="Screenshot 2025-10-07 101737" src="https://github.com/user-attachments/assets/1fb24e32-bf68-40d5-af6c-3cd491b05946" />
<img width="1892" height="950" alt="Screenshot 2025-10-07 103221" src="https://github.com/user-attachments/assets/60265074-0f3d-4422-b527-d0815df27576" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



