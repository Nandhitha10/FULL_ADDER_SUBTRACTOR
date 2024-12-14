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
![Screenshot 2024-12-14 194000](https://github.com/user-attachments/assets/6379f514-10e8-489b-a2e9-2417561db33d)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
![Screenshot 2024-12-14 194236](https://github.com/user-attachments/assets/9b209432-b184-47b3-9e03-6bb67472594e)

**Truthtable**
FULL ADDER
![Screenshot 2024-12-14 194256](https://github.com/user-attachments/assets/6425b4a7-a62a-4438-83d3-ec3ac4eaf76b)

FULL SUBTRACTOR
![Screenshot 2024-12-14 194313](https://github.com/user-attachments/assets/7d4206ab-050e-47c1-ba24-88443dd0353a)

**Procedure**

Write the detailed procedure here

**Program:**
FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule

FULL SUSTRACTOR


module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: NANDHITHA S RegisterNumber:24900454
*/

**RTL Schematic**
FULL ADDER
![Screenshot 2024-12-14 194418](https://github.com/user-attachments/assets/3fd76eef-f11b-40ed-ba3c-5e4753073ce8)
FULL SUBTRACTOR
![Screenshot 2024-12-14 194426](https://github.com/user-attachments/assets/f24dc9d3-3039-4658-898a-62f82ef9a8a4)

**Output Timing Waveform**
FULL ADDER
![Screenshot 2024-12-14 194454](https://github.com/user-attachments/assets/59a7260f-345a-4ee0-b7bf-2278656f1659)

FULL SUTRACTOR
![Screenshot 2024-12-14 194512](https://github.com/user-attachments/assets/59df1e4a-552d-4b9e-8b09-2d0288cf37d2)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



