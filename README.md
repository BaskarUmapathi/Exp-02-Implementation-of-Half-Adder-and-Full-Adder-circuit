## Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

## Implementation-of-Half-Adder-and-Full-Adder-circuit
# AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

# Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

# Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

# Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
# Program:
# Half Adder
module halfadder(sum,a,b,carry);

```
input a,b;
output sum,carry;
xor (sum,a,b);
and (carry ,a,b);
endmodule
```



# RTL realization
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/3f26367f-6507-4e08-9d59-814e588d0172)

# Truth Table
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/368428f8-529a-4f97-8cd5-237bce9b2c5f)

# Waveform
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/0941ac8d-0e19-447b-b0da-b6399c7c26d7)

# Program
# Full Adder
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum, carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```
# RTL realization
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/d27efe31-2a0d-4f4a-830e-0ca2cf976e6b)

# Truth Table
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/60535c47-81c3-4d1e-af06-8d1afc6e03d2)

# Waveform
![image](https://github.com/vasanthkumarch/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151434098/09cf67d5-f26d-4ce3-8502-e017261ffebb)
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: BASKAR U
RegisterNumber:  212223220013
*/

# Result:
Thus the given full adder and half adder are verified using verilog programming.









### Result:
