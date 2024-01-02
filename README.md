# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
### Program
### Half Adder
```
module halfadder(sum,a,b,carry);
input a,b;
output sum,carry;
xor (sum,a,b);
and (carry ,a,b);
endmodule 
```
/* Program to design a half adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: BASKAR U 

RegisterNumber: 212223220013
*/
### RTL realization
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/a15f6af3-852e-4566-820c-32adbdb40e47)

### Truth Table 
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/9cdb7679-ee8d-45d5-87bd-c15c557572a5)

### Waveform
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/61347188-bf11-4289-b786-8ee60577a7ed)

### Full Adder
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum, carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule 
```
/* Program to design a full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: BASKAR U

RegisterNumber: 212223220013
*/
### RTL realization
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/b2933bc2-bff4-4f03-bef4-1d00aa5aba87)

### Truth Table
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/8cde127c-a04a-4815-89fd-3e50cd10ad74)

### Wavwform
![image](https://github.com/BaskarUmapathi/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/62719ed2-9e27-45b7-8132-3f04c1cf7bb5)


### Result:
Thus the given full adder and half adder are verified using verilog programming.

