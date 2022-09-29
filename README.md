# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Gayathri A
RegisterNumber: 212221230028

using NAND:
   ```
   module combo1(a,b,c,d,f);
   
   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=(~c & b & a);
   
   assign q=(~d & c & ~a);
   
   assign r=(c & ~b & a);
   
   assign f=(~(~p & ~q & ~r));
   
   endmodule
```
using NOR:
   ```
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
*/
## RTL realization

## Output:

NAND:

## RTL

![de4 1](https://user-images.githubusercontent.com/94154854/193058911-1b0b8f82-bde1-4c69-8f21-27fcf37d1824.png)

## Timing Diagram

![ex4 2](https://user-images.githubusercontent.com/94154854/193058946-a105f704-8f3d-4b64-9e85-aef4a49d8bf2.png)

## Truth Table

![ex4 6](https://user-images.githubusercontent.com/94154854/193070445-f2a04823-ce6f-46da-bd10-ec1a5e54a025.png)


NOR:

## RTL:

![ex4 3](https://user-images.githubusercontent.com/94154854/193068545-daf9cf66-fc88-4b00-a393-4ffbac082090.png)


## Timing Diagram:

![ex4 4](https://user-images.githubusercontent.com/94154854/193069187-9860a725-845d-426d-9bf7-87f5b1f39e96.png)


## Truth Table:

![ex4 7](https://user-images.githubusercontent.com/94154854/193070747-02a10b19-554b-4d48-996b-deb3daf2c284.png)



## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
