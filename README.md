# Exp-03 Implementation of Half Adder and Full Adder circuit

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
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sabari Akash A
RegisterNumber: 212222230124 
```
```
Half Adder:
module halfadder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum=A^B;
assign carry=A&B;
endmodule
```
```
Full Adder:
module Fulladder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
```
## Output Waveform:
### Half Adder:
![Screenshot 2023-09-01 084945](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/df8c47c7-743e-43ce-b9bf-b65de203e935)
### Full Adder:
![Screenshot 2023-09-01 091219](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/b6bfaa14-2e76-47dd-b18f-ee3490fa2703)

## RTL DIAGRAM:
### Half Adder:
![Screenshot 2023-09-01 084415](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/b140583c-4278-41d9-aeca-3c8c12143eed)
### Full Adder:
![Screenshot 2023-09-01 085635](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/f1ee68dc-3f13-4034-9891-d475e263f70e)
## TRUTH TABLE 
### Half Adder:
![Screenshot 2023-09-01 092457](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/a20b8f13-a65c-41ce-816e-960026574f46)
### Full Adder:
![Screenshot 2023-09-01 093111](https://github.com/Sabariakash22009103/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119390227/60ea1f9b-1a0d-4cac-8df5-634db3638782)
### Result:
Thus the half adder and full adder circuits are designed and the truth tables is verified using quartus software.
