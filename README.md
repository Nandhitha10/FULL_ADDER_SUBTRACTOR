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
![Screenshot 2024-12-14 194000](https://github.com/user-attachments/assets/28d97453-1623-4334-9a05-9d2bb5532a1b)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
![Screenshot 2024-12-14 194236](https://github.com/user-attachments/assets/8472cfb3-7a79-458e-b16e-70cc01e0442b)

**Truthtable**
FULL ADDER
![Screenshot 2024-12-14 194256](https://github.com/user-attachments/assets/32a9d89c-1f2c-4f1e-8a1f-6c7847249f49)
FULL SUBTRACTOR
![Screenshot 2024-12-14 194313](https://github.com/user-attachments/assets/b8b9c69d-8085-461d-acf1-0b24d4fdec89)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/FULL ADDER

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

**RTL Schematic**
FULL ADDER 
![Screenshot 2024-12-14 194418](https://github.com/user-attachments/assets/314e0c3e-3f1c-4544-864d-70e43824cfbf)

FULL SUBSTACTOR

![Screenshot 2024-12-14 194426](https://github.com/user-attachments/assets/53ae6d62-ce36-457d-b6bf-ce46c2ff3395)


**Output Timing Waveform**
FULL ADDER
![Screenshot 2024-12-14 194454](https://github.com/user-attachments/assets/842c7a8f-94b8-43e9-9e29-970f58b19844)


FULL SUBTRACTOR
![Screenshot 2024-12-14 194512](https://github.com/user-attachments/assets/1a7576db-a702-463a-8f1c-498279628604)
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



