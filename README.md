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
![WhatsApp Image 2024-12-06 at 04 40 13_d219bef1](https://github.com/user-attachments/assets/e9e7c805-40aa-45b5-91d6-d09191433283)

**Full Subtractor**
![WhatsApp Image 2024-12-06 at 04 40 44_411b3e0e](https://github.com/user-attachments/assets/0982113c-cbf0-4107-9808-0b4ac3253d54)


A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**



**Procedure**

Write the detailed procedure here

**Program:**
````
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:24900650 
RegisterNumber:subashree karthikeyan*/
````
```
module EXP04(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```
```
module EXP04 (df,bo,a,b,bin);
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

**RTL Schematic**
![WhatsApp Image 2024-12-06 at 04 42 05_73882d7f](https://github.com/user-attachments/assets/24ad7d06-c23c-4789-9854-1fac4dd599f5)
![WhatsApp Image 2024-12-06 at 04 42 45_eef8390f](https://github.com/user-attachments/assets/3402546b-ef28-4a8f-a370-5083eafb20d7)

**Output Timing Waveform**

![WhatsApp Image 2024-12-06 at 04 43 26_c4872b67](https://github.com/user-attachments/assets/73740b37-0288-423e-b27e-8f80a8d83107)


![WhatsApp Image 2024-12-06 at 04 44 09_87c1e75e](https://github.com/user-attachments/assets/f569bb3c-86b1-4dd2-aaf1-c8127ed853a0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



