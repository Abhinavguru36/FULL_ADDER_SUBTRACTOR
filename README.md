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
~~~
module exfull (a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor g1(sum,a,b,c);

assign carry =(a&b)|(b&c)|(c&a);

endmodule

full subtractor module fullsub(a,b,c,diff,borrow);

input a,b,c;

output diff,borrow;

xor g1(diff,a,b);

assign borrow =(b&c)|(~a&c)|(~a&b);

endmodule
~~~
Developed by:ABHINAV GURU R RegisterNumber:25016474


**RTL Schematic**
<img width="1864" height="934" alt="image" src="https://github.com/user-attachments/assets/657548a4-5ef8-4d68-9df1-fb311f07746d" />
<img width="1912" height="954" alt="image" src="https://github.com/user-attachments/assets/618ff97b-8e09-41d8-af63-818307a24837" />



**Output Timing Waveform**
<img width="1910" height="993" alt="image" src="https://github.com/user-attachments/assets/db5015dc-30a3-433d-bd39-8335b5979ccc" />
<img width="1898" height="964" alt="image" src="https://github.com/user-attachments/assets/6091468e-df57-4e62-ae2c-e6e9800f054a" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



