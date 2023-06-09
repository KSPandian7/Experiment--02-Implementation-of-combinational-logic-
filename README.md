# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

## Procedure
.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results. Program:.
## Program:
```python
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: KULASEKARAPANDIAN K
RegisterNumber:  212222240052

module ff(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);
endmodule

module de (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule
```

## Output:
## RTL realization


![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/7660769c-b026-4474-8cec-64345ae2c53d)

![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/177f7625-67b5-4fbe-9ded-9894155ffeb9)


## Timing Diagram

![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/2e02ee6a-37ce-4414-8a0d-ce76041e864f)

![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/d89377d2-e677-4ce7-80b2-61029acca376)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
