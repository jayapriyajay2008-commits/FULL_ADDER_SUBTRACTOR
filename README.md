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
Full adder

<img width="474" height="388" alt="image" src="https://github.com/user-attachments/assets/fb603126-f983-4f46-a30b-c1949bf1030c" />

Full subractor

<img width="453" height="316" alt="image" src="https://github.com/user-attachments/assets/da52e6de-c824-4eab-8d42-b7f558c4fc1f" />

**Procedure**

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

**RTL Schematic**
Full adder
<img width="816" height="404" alt="image" src="https://github.com/user-attachments/assets/e52622af-dc11-48a6-8cd4-e90ee3c6d1ae" />
Full subractor
<img width="810" height="395" alt="image" src="https://github.com/user-attachments/assets/92bda9de-659a-4784-9c87-7ae9ad4cc76f" />

**Output Timing Waveform**
Fulladder
<img width="787" height="405" alt="image" src="https://github.com/user-attachments/assets/23e9aed9-4b8f-4334-869a-b4bd8b66f1ff" />
full subractor
<img width="775" height="384" alt="image" src="https://github.com/user-attachments/assets/d236b89f-f9be-4295-b556-307953a74a6e" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



