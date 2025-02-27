# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit
Implementation-of-Half-Adder-and-Full-Adder-circuit
### Name: Loshini.G
### Reference No: 212223220051
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
#### Hardware – PCs, Cyclone II , USB flasher
#### Software – Quartus prime

## Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

## Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

## Figure -02 FULL ADDER 

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Loshini.G
RegisterNumber: 212223220051

half adder:
module halfadd(sum,carry,a,b);
input a,b;
output sum,carry;
assign sum=a^b;
assign carry=a&b;
endmodule

full adder:
module fulladd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule
```
## Truthtable:

Half adder:
![image](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/09275da0-b001-4f51-b318-862d58141382)

Full adder:
![image](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/375b3b01-9284-406f-810f-222fc5183610)

## RTL realization:

Half adder:
![half add rtl](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/8e573e54-72af-47b2-be0a-7296dced9b3d)

Full adder:
![fulladd rtl](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/3e7ee0ff-cc91-4a12-85a9-5a215acbc948)

## TIMING DIAGRAM:

Half adder:
![half add wf](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/3480265a-1222-4147-a895-dc034ae1979a)

Full adder:
![full wf](https://github.com/Loshini2301/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/150007305/f03c7d52-474b-4c4e-a69c-4ac26837bca5)

### Result:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming
