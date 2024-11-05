# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**<br>
![WhatsApp Image 2024-11-05 at 11 32 19_51b36444](https://github.com/user-attachments/assets/e3880bff-413e-4c28-ac1d-e2dae089ff9b)


Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**
![WhatsApp Image 2024-11-05 at 11 32 19_8bdeeb7a](https://github.com/user-attachments/assets/acc594aa-ba43-4443-8685-957675f9c635)


The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subractor


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module exp3(a,b,cy, sm, df,bo);
 input a,b;
 output sm,cy, df, bo;
 xor(sm,a,b); 
 and(cy,a,b); 
 xor(df,a,b);
 and (bo,~a,b);
 endmodule
```

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: DHANUSH M.D RegisterNumber:24900042

**RTL Schematic**
![Screenshot 2024-11-05 103505](https://github.com/user-attachments/assets/6d341947-9583-4ef8-ae16-5245927cecd4)

**Output/TIMING Waveform**
![Screenshot 2024-11-05 104225](https://github.com/user-attachments/assets/655547ef-872b-4104-a115-560d36bf74e3)

**Result:**
the truth table for half adder and half subtractor are verified successfully
