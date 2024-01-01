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
### 
Program:
halfadder
````
module halffull(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
````
RTL
![image](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/13c0a9a5-917f-4df2-a8d9-e89deb5ecd05)
TRUTH TABLE
![WhatsApp Image 2024-01-01 at 20 17 23_320655be](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/a30c5e28-0153-4390-a078-b5eb3f6814db)
WAVEFORM
![Screenshot 2023-12-31 132251](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/6d3dc34c-acc2-420a-8d17-de7fdaf827fb)


full adder
````
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule 
````
RTL
![image](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/38f5f9cc-226c-4250-8060-854ca1b55b97)
TRUTHTABLE
![WhatsApp Image 2024-01-01 at 20 17 23_fbc6862b](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/ec073fcc-dbdc-4323-ae74-ce58b39a3f20)
WAVEFORM
![Screenshot 2024-01-01 195253](https://github.com/SGokul2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147121825/e1f3e256-96ba-4f69-82b3-1542c1c03b37)


/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/
Logic symbol & Truthtable
RTL realization

### Output:
### RTL
### TIMING DIAGRAM


### TRUTH TABLE 

### Result:
