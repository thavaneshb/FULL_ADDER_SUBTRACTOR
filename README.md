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

**Procedure**

Full Adder:

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

Full Subtractor:

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.


**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: B.THAVANESH

RegisterNumber: 24900957

**FULL ADDER**

```
module fa(a, b, cin, sum, carry);
  input a, b, cin;
  output sum, carry;
  
  assign sum = (a ^ b ^ cin);
  assign carry = (a & b) | (cin & (a ^ b));
endmodule

```

**FULL SUBTRACTOR**

```
module fs(a,b,Bin,Borrow,Difference);
input a,b,Bin;
output Borrow,Difference;
assign Difference = a ^ b ^ Bin;
  assign Borrow = (a & b) | ((a ^ b) & Bin);
endmodule
```

**RTL Schematic**

**FULL ADDER**

![image](https://github.com/user-attachments/assets/221ffc4d-c6e3-466a-ad79-a62500a846f2)

**FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/a513337e-d02a-43bf-82de-d35df06e6b94)


**Output Timing Waveform**


**FULL ADDER**
![image](https://github.com/user-attachments/assets/54dc96cb-c166-456d-9456-b671398ea12c)


**FULL SUBTRACTOR**
![image](https://github.com/user-attachments/assets/b958a505-6eef-4281-96b6-19b77ef441e2)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



