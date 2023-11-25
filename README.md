# Experiment--02-Implementation-of-combinational-logic
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime

## Theory:
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

OR Gate:
The OR gate is a fundamental digital logic gate that operates on two binary inputs, producing an output of 1 if at least one input is 1. It symbolizes logical disjunction and is essential in building logical circuits and decision-making processes in computers and electronics.

AND Gate:
The AND gate is a fundamental digital logic gate with two inputs and one output. It produces a high output (1) only when both input signals are high (1). If any input is low (0), the output remains low. It's a building block for more complex logic circuits and is integral in digital computations.

NOT Gate:
The NOT gate is a fundamental digital logic gate. It has a single input and a single output. The output is the inverse of the input: if the input is high (1), the output is low (0), and vice versa. It's a basic building block in digital circuits, used for logic inversion.

## Procedure:
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Divya M
RegisterNumber: 23013162
```
module EX02DE(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1=(~a&(~b)&(~c)&(~d));
assign A2=(a&c&(~d));
assign A3=((~b)&c&(~d));
assign A4=(~a&b&c&d);
assign A5=(b&(~c)&d);
assign F1=A1|A2|A3|A4|A5;
assign B1=(x&(~y)&z);
assign B2=(~x&(~y)&z);
assign B3=(~w&x&y);
assign B4=(w&(~x)&y);
assign B5=(w&y&z);
assign F2=B1|B2|B3|B4|B5;
endmodule
```
*/
## RTL realization:
![Screenshot (179)](https://github.com/DivyaMunirathnamm/Experiment--02-Implementation-of-combinational-logic-/assets/147474097/29106b3d-a463-4451-8b1d-7e04d4e19d2f)
![Screenshot (180)](https://github.com/DivyaMunirathnamm/Experiment--02-Implementation-of-combinational-logic-/assets/147474097/b75229a4-a95a-47a6-9c43-eb70ebce671f)

## Timing Diagram:
![Screenshot (181)](https://github.com/DivyaMunirathnamm/Experiment--02-Implementation-of-combinational-logic-/assets/147474097/3679f249-83c4-42fd-b61d-ff0457f0725a)

## Truthtable:

![Screenshot (182)](https://github.com/DivyaMunirathnamm/Experiment--02-Implementation-of-combinational-logic-/assets/147474097/8519dd1c-bd0c-46b6-a19e-5d2a1fa941f7)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
