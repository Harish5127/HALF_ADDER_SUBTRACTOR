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

  Half Adder
  
![Screenshot 2024-12-04 001225](https://github.com/user-attachments/assets/564c5a47-0c27-47be-a374-a1f1026edd6e)

  Half Subtractor
  
![Screenshot 2024-12-04 001231](https://github.com/user-attachments/assets/d1803677-d703-42ac-b824-f9bb0f8450d5)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Harish R
RegisterNumber: 24001191
*/
```
 Half Adder
```
module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum= (a ^ b);
assign carry= ( a & b);
endmodule
```
 Half Subtractor
```
module hs(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a ^ b);
assign borrow= ( ~a & b);
endmodule
```

**RTL Schematic**

 Half Adder
 
![Screenshot 2024-12-03 235613](https://github.com/user-attachments/assets/f291159d-55ba-4be4-b1d9-c95d4f67a458)

 Half Subtractor
 
![Screenshot 2024-12-04 000143](https://github.com/user-attachments/assets/8c55bea4-dde5-44ad-abb7-05e143419d78)


**Output/TIMING Waveform**

 Half Adder
 
![Screenshot 2024-12-03 235735](https://github.com/user-attachments/assets/c9f74bf9-311b-4567-b06e-b446753c5ffc)
 Half Subtractor
 
![Screenshot 2024-12-04 000253](https://github.com/user-attachments/assets/affe7941-f0b2-466e-82ea-9aebcf55a7fd)


**Result:**

Thus the output of half adder and half subtractor circuit are verified its truth table in Quartus using Verilog programming.
