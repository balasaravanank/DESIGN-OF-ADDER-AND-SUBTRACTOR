# FULL_ADDER_SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![WhatsApp Image 2025-04-22 at 10 43 17_517cb463](https://github.com/user-attachments/assets/3e1620d1-e2a9-4387-be27-54bdfb65c856)


![WhatsApp Image 2025-04-22 at 10 43 18_88f9e932](https://github.com/user-attachments/assets/0d1a306f-1de5-49b2-a6a9-6f9da6816c1a)

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**
~~~python

module exp3(a,b,cin,bin,sum_a,cout,diff_s,borr_s);
input a,b,cin,bin;
output sum_a,cout,diff_s,borr_s;
assign sum_a=a^b^cin;
assign cout=(a^b)&cin |(a&b);
assign diff_s=a^b^bin;
assign borr_s=(~a&~b&~bin)|(~a&b&~bin)|(~a&b&bin)|(a&b&bin);
endmodule

~~~
Developed by : BALA SARAVANAN K

Register Number : 212224230031

**RTL Schematic**

![Screenshot 2025-04-22 110015](https://github.com/user-attachments/assets/0d03043d-4aa8-4a7a-bc7a-546b3e658188)

**Output Timing Waveform**
![WhatsApp Image 2025-04-22 at 11 15 39_e8bba4be](https://github.com/user-attachments/assets/e083f2b0-aa7f-410e-beeb-bd6d2bc3898e)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


