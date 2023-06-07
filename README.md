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

Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Lokesh kumar P
RegisterNumber:  212222110021


F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
```

## RTL realization

# output:
```
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![233444435-4818a840-64c2-483b-a579-1e721d4a128e](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--02-Implementation-of-combinational-logic-/assets/119644432/3905b57b-1971-4a7e-aa76-716a04f08317)

F2=xy’z+x’y’z+w’xy+wx’y+wxy
![233444228-a12416d9-cc9c-4d53-8da7-1eb39e636955](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--02-Implementation-of-combinational-logic-/assets/119644432/9e6c9525-0797-48fb-8170-0ac14674e148)


## Timing Diagram

# FOR NAND:
![233448490-bde5a4e7-3465-45cb-8e95-49a796d61035](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--02-Implementation-of-combinational-logic-/assets/119644432/59a60755-8ebc-4782-b578-e01820242609)


## FOR NOR:
![233446842-1ef9acbf-a8d4-459f-a747-f5e7aae8e322](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--02-Implementation-of-combinational-logic-/assets/119644432/769b79ba-50f2-4726-9716-4609e2f3c6cf)

```

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
