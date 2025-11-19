# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

half adder:

![WhatsApp Image 2025-11-19 at 10 42 11_1947c1a6](https://github.com/user-attachments/assets/c6c7cd4a-59a2-4a28-aba6-50678c7d56c5)

half subractor:

![WhatsApp Image 2025-11-19 at 10 42 05_1633cbbc](https://github.com/user-attachments/assets/eb4c53c2-1525-4102-beff-8ee798de9a6c)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**


half adder:
~~~
module halfadder(a,b,s,c);
input a,b;
output s,c;
xor g1(s,a,b);
and g2(c,a,b);
endmodule
~~~

half subractor:
~~~
module halfsub(a,b,diff,bo);
input a,b;
output diff,bo;
assign diff=a^b;
assign bo=(~a)&b;
endmodule 
~~~

**RTL Schematic**

half adder:

<img width="796" height="496" alt="ex 3 1" src="https://github.com/user-attachments/assets/fb7db6db-f07a-4f4d-9125-b507b31d728d" />

half subractor:

<img width="1003" height="526" alt="ex 4 1" src="https://github.com/user-attachments/assets/e90170d6-633d-4572-aea8-8dee4ae8b5c8" />

**Output/TIMING Waveform**

half adder:

<img width="1920" height="1119" alt="ex3 1" src="https://github.com/user-attachments/assets/bf1a214b-057f-465d-8643-2ecbf6795cdd" />

half subractor:

<img width="1920" height="1131" alt="ex4 1" src="https://github.com/user-attachments/assets/eb9a33de-6861-428c-87ca-5f0682b0dfec" />

**Result:**

Thus the half adder and half subtractor circuits were successfully designed, and their truth tables were verified in Quartus using Verilog programming.
