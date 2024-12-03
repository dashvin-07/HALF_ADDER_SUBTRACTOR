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

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Dashvin S
RegisterNumber:24901048
*/
## Half adder
```
 
module ha_dataflow(a, b, s, ca); 
    input a; 
    input b; 
    output s; 
    output ca; 
  assign#2 s=a^b; 
  assign#2 ca=a&b; 
endmodule
```
## Half subtractor
```
 
module hs_dataflow(a, b, dif, bor); 
    input a; 
    input b; 
    output dif; 
    output bor; 
  wire abar; 
  assign#3 abar=~a; 
  assign#3 dif=a^b; 
  assign#3 bor=b&abar; 
endmodule
```

**RTL Schematic**
## Half adder
![half adder](https://github.com/user-attachments/assets/c1afcd0c-e7ba-4740-97b7-c1d6a37ded8c)
## half subtractors
![half substractor](https://github.com/user-attachments/assets/c67a214f-ba19-4768-9d4d-e16b3e90c2e8)

**Output/TIMING Waveform**
## Half adder
![half adder op](https://github.com/user-attachments/assets/123ae70d-6cfe-4dc0-8e7b-1d6c3ed3b672)

## Half subtractors
![half subtractors op](https://github.com/user-attachments/assets/aade2939-97a7-4234-ac82-fa8dc8fc9eef)

**Result:
Thus the half subracter and half adder circuits are design and the truth tables are verified using quartus software
