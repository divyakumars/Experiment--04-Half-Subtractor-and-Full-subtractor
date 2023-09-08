NAME:DIVYA K
REGISTER NUMBER:212222230035

# Experiment 04 Half Subtractor and Full subtractor
## Implementation of Half subtractor and Full subtractor circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
#### 1.Use module projname(input,output) to start the Verilog programmming.
#### 2.Assign inputs and outputs using the word input and output respectively.
#### 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
#### 4.Use each output to represnt onre for differnce and the other for borrow.
#### 5.End the verilog program using keyword endmodule


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: DIVYA K
RegisterNumber:212222230035
```
```

module exo4(A,B,diff,borrow);
input A,B; output diff,borrow;
wire X;
xor(diff,A,B);
not(X,A);
and(borrow,X,B);
endmodule

```
```
module fullsub(A,B,bin,diff,borrow);
input A,B,bin;
output diff,borrow;
assign diff = A^B^bin;
assign borrow =(~A&B)|(~(A^B))&bin;
endmodule
```


## Truthtable


.![167161887-f0590beb-3f4e-43ed-8a68-8c072a46fb81](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/8c4746dc-7059-421b-81bd-37a679cfe19d)

![167162027-0c5225fb-1400-4d6a-9f16-18bbf6789916](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/c491837e-8e1d-4171-a570-19f8905e0c58)

##  RTL diagram
![RTL](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/1ae42980-1661-4b03-8c2b-f873eee49582)

![image](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/b8922232-c142-420b-ac15-5c5cffc5a214)



## output waveform

![image](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/7a8b57e1-d724-4614-81f3-306f4e484793)



![image](https://github.com/divyakumars/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/119393621/62a29b2d-52f6-486d-a1bc-c049b0a4f272)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

