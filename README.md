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
Logic gates are electronic circuits which perform logical functions on one or more inputs
to produce one output.

## USING NAND GATES:
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT
gate. So its output is complement of the output of an AND gate.This gate can have
minimum two inputs, output is always one. By using only NAND gates, we can realize all
logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal
gate. First note that the entire expression is inverted and we have three terms ANDed. This
means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND
expression. Finally, negated single terms can be generates with a 2-input NAND gate
acting as an inverted.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## USING NOR GATES:
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed
by NOT gate. So its output is complement of the output of an OR gate. This gate can have
minimum two inputs, output is always one. By using only NOR gates, we can realize all
logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal
gate. Designing a circuit with NOR gates only uses the same basic techniques as designing
a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only
difference between NOR gate design and NAND gate design is that the former must
eliminate product terms and the later must eliminate sum terms.
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
![D0](https://user-images.githubusercontent.com/119644432/233999418-318ac286-3cc1-4ac4-a7d6-3507012ffb28.png)

## Procedure
Step 1: Create a project with required entities.

Step 2: Create a module along with respective file name

Step 3: Run the respective programs for the given boolean equations.

Step 4: Run the module and get the respective RTL outputs.

Step 5: Create university program(VWF) for getting timing diagram.

Step 6: Give the respective inputs for timing diagram and obtain the results.

Program to implement the given logic function using NAND and NOR gates and to verify
its operations in quartus using Verilog programming.

## Program:
```
Program to implement the given logic function using NAND and NOR gates and to
verify its operations in quartus using
Verilog programming.
Developed by: LOKESH KUMAR P
RegisterNumber: 212222240054

Using NAND gates:
module NAND(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P=(~(~C & B & A));
assign Q=(~(~D & C & A));
assign R=(~(C & ~B & A));
assign F=~(P & Q & R);
endmodule

Using NOR gates:
module NOR(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = (C & ~B & A);
assign Q = (D & ~C & A);
assign R = (C & ~B & A);
assign S = (~(P | Q | R));
assign F = (~S);
endmodule

## RTL realization

# output:
## RTL FOR NAND GATE:
```
![D1](https://user-images.githubusercontent.com/119644432/234000563-33b4a7ec-8338-4cea-ace0-5742ff68a4b7.png)

## FOR NOR:
![D2](https://user-images.githubusercontent.com/119644432/234000724-4717d02d-c71c-4754-9bd5-d17bcb1eb004.png)

## Timing Diagram

# FOR NAND:
![D3](https://user-images.githubusercontent.com/119644432/234000926-3e93994c-495c-4145-96e8-0dd817667e98.png)

## FOR NOR:
![D4](https://user-images.githubusercontent.com/119644432/234001001-fc39914f-3237-4b7d-94fc-8da320aecb72.png)
```

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
