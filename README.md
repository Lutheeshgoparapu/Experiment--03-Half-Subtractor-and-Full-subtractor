# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
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

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.




## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: GOPARAPU LUTHEESH
RegisterNumber:  212221230029
```
## HAF SUBTRACTOR
```
module burrow(output B,D, input X,Y);
assign D = (X ^ Y);
assign B = (~X & Y);
endmodule
```
##FULL SUBTRACTOR
```
module sub(X,Y,Z,B,D);
input X,Y,Z;
output B,D;
assign D = (X^Y^Z);
assign B = (~X&(Y^Z)|(Y&Z));
endmodule
```

## Output:

## Truthtable
### Hald subtractor

![01](https://user-images.githubusercontent.com/94154531/192447593-3e666b64-933d-43bf-84e0-31e95d972643.jpg)

### Full Subtractor
![192192425-c0cb9528-9c00-4fae-831f-9211828203e5](https://user-images.githubusercontent.com/94154531/192447718-6c6873d9-c373-4bb3-99bf-4b1b35e6aa5a.jpg)



##  RTL realization
### Half Subtractor
![192192173-db5363d6-2039-4175-beb6-852285a03201](https://user-images.githubusercontent.com/94154531/192447792-7eb2b1e1-4922-474b-be9c-620ce9045410.jpg)
### Full SUbtractor
![192192181-c691c22c-cdc6-4913-b3e7-123341a13323](https://user-images.githubusercontent.com/94154531/192447853-34f58fb5-3b46-4a32-a3c3-3f30e0c1bbd1.jpg)




## Timing diagram 
### Half Subtractor
![192192162-1cb64c7d-dc3a-4ed3-8820-bc3b122c2f72](https://user-images.githubusercontent.com/94154531/192447918-b901f65a-e5e0-47de-ada9-f25f18df802c.jpg)
### Full Subtractor
![192192153-19868b77-5569-45ca-b8f2-46e5fa39c8ea](https://user-images.githubusercontent.com/94154531/192447983-f35187b7-4fbf-4510-9793-adf6d6a37212.jpg)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
