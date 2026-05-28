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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:R.Divyadharshini RegisterNumber:212225230062
*/
```
module EXP4FULLADDER(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
```
```
module EXP4FULLSUBTRACTOR(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
```
**RTL Schematic** FULL ADDER 
<img width="1072" height="581" alt="Screenshot 2026-05-28 180841" src="https://github.com/user-attachments/assets/d1b55ee7-3276-403b-a708-8e350834e00b" />

FULL SUBSTRACTION 


<img width="1076" height="561" alt="Screenshot 2026-05-28 180857" src="https://github.com/user-attachments/assets/bcc0f175-4002-4552-b356-ba9a54b86893" />
   

**Output Timing Waveform** FULL ADDER
<img width="1056" height="574" alt="Screenshot 2026-05-28 181028" src="https://github.com/user-attachments/assets/f340c081-0e11-43d3-a5ca-b852cf6bc571" />

<img width="1066" height="571" alt="Screenshot 2026-05-28 181132" src="https://github.com/user-attachments/assets/e5bf9462-d5f9-4d0a-b24d-4fcdb905eef6" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



