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

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
Developed by: Vineesh.M
RegisterNumber:  212221230122
```

```
HALF ADDER:

module ex2(A,B,Cin,S,Cout);
input A,B,Cin;
output S,Cout;
wire D,E,F;
xor(D,A,B);
xor(S,D,Cin);
and(E,Cin,D);
and(F,A,B);
or(Cout,E,F);
endmodule

FULL ADDER:

module ex2(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
Logic symbol & Truthtable
RTL realization
### Output:
### HALF ADDER:
### RTL:
![de1](https://user-images.githubusercontent.com/93427254/230759489-16f625e1-7860-4e00-8456-54067e1fd7b0.png)
### TIMING DIAGRAM:
![de2](https://user-images.githubusercontent.com/93427254/230759505-1b5253fd-6010-4312-afb7-e41e1f58914f.png)
### TRUTH TABLE:
![de3](https://user-images.githubusercontent.com/93427254/230759515-4acd80aa-0482-487c-a452-264d4efefe06.png)
### FULL ADDER:
### RTL:
![de4](https://user-images.githubusercontent.com/93427254/230759554-6c47d911-1ac3-43fb-bbb3-e14d0d1c87bc.png)
### TIMING DIAGRAM:
![de5](https://user-images.githubusercontent.com/93427254/230759559-ddb2598f-ca50-4b1d-9c17-a853169a2e75.png)
### TRUTH TABLE:
![de6](https://user-images.githubusercontent.com/93427254/230759560-86740eed-bb17-49f5-8606-3afb7b86db05.png)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
