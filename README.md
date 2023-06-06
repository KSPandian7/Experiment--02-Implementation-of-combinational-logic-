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

## Using NAND gates:
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR Gates:
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```python
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: KULASEKARAPANDIAN K
RegisterNumber:  212222240052

USING NAND:
   module combo1(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=(~c & b & a);
   assign q=(~d & c & ~a);
   assign r=(c & ~b & a);
   assign f=(~(~p & ~q & ~r));
   endmodule

USING NOR:
   module combo2(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=( c & ~b & a);
   assign q=( d & ~c & a);
   assign r=( c & ~b & a);
   assign f=(~(~( p | q | r)));
   endmodule
```

## Output:

## USING NAND GATE:

## RTL realization
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/e71a2e3f-2b9e-4d5c-94c0-3c829da9e2e1)

## Timing Diagram
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/eedfdab3-961a-487e-8619-a00eb65fa76f)

## TRUTH TABLE:
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/24fe1599-ad4c-466f-9f6a-933e0d978501)

## USING NOR:

## RTL realization
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/27d9ea55-0186-41f6-8928-c1adb6a5dd65)

## Timing Diagram :
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/3f14e211-f92a-4ab8-a9e6-a22112ae0e6d)

## TRUTH TABLE :
![image](https://github.com/KSPandian7/Experiment--02-Implementation-of-combinational-logic-/assets/113496887/3f797e7a-c4fb-4aac-8a42-b47ba8fa076b)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
