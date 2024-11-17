Name: A Ahil Santo

Register Number: 24900087

# EXP3: HALF ADDER AND SUBTRACTOR

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

**Half Adder**

![ha truthtable](https://github.com/user-attachments/assets/e645e07f-f76b-498c-96d3-34508f909ba4)


**Half Subtractor**

![hs_truthtable](https://github.com/user-attachments/assets/ce483827-8f26-4ab8-b45e-4901325db982)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

**Half Adder**

```
module hadd(a,b,sum,cout);
input a,b;
output sum,cout;
xor g1(sum,a,b);
and g2(cout,a,b);
endmodule 
```

**Half Subtractor**

```
module hsub(a,b,sub,bout);
input a,b;
output sub,bout;
wire w1;
xor g1(sub,a,b);
not g2(w1,a);
and g3(bout,w1,b);
endmodule 
```

**RTL Schematic**

**Half Adder**

![Screenshot 2024-11-15 133559](https://github.com/user-attachments/assets/16aa1d41-21e2-4c1a-8725-2dd6dd3292ec)


**Half Subtractor**

![123](https://github.com/user-attachments/assets/ecda5c64-2b36-4526-8037-66be4096cf8b)


**Output/TIMING Waveform**

**Half Adder**

![Screenshot (9)](https://github.com/user-attachments/assets/5c683293-f5a3-4a97-a5fc-ece59af63f49)

**Half Subtractor**

![Screenshot (12)](https://github.com/user-attachments/assets/30691d93-290f-4e59-85a8-ccd7ea266467)


**Result:**

The half adder and half subtractor circuits were successfully designed, and their truth tables were verified in Quartus using Verilog programming.


