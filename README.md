# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: DINESHKARTHIK N
RegisterNumber:  23013921
*/
## Half adder:
module Halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

## Full adder:
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b) | (b&c) | (c&a));
endmodule

Logic symbol & Truthtable
RTL realization

### Output:
### RTL:
Halfadder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/68490ba1-b646-4786-873f-9bf38f7cdd0b)

Fulladder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/7b9ee8e5-46be-42b0-9935-4fa4ccd5ad0d)


### TIMING DIAGRAM
Halfadder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/e7cbbd24-7bce-4fa9-b9b5-e8c77a2f6833)

Fulladder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/7b059255-20b9-4274-b239-e498a081bd30)


### TRUTH TABLE 
Halfadder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/771bb659-e828-471b-b4df-4460b5df6fd6)

Fulladder:
![image](https://github.com/dinesh2068/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151390189/ef60d4d7-23e2-4450-8795-d7f08b83d0ce)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
