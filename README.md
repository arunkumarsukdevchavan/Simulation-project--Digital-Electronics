# TITTLE
DESIGN AND SIMULATE 6 BIT BINARY TO GREY CONVERTER USING VERILOG
# THEORY
The 6-bit binary to Gray code conversion involves converting a 6-bit binary number into its corresponding Gray code representation. Gray code is a binary numeral system where adjacent codes differ by only one bit.

Here's a theory about how a 6-bit binary to Gray code converter could work:

The 6-bit binary number is represented by six input bits, labeled as B5, B4, B3, B2, B1, and B0, where B5 is the most significant bit and B0 is the least significant bit.

To convert the binary number to Gray code, we start with the most significant bit (B5) and perform the following steps for each subsequent bit:

Take the current bit and XOR (exclusive OR) it with the next higher significant bit. For example, to convert B4 to Gray code, we XOR B4 with B5.
Assign the result to the corresponding Gray code bit. For example, if the XOR operation between B4 and B5 yields G4, then G4 is the Gray code representation of B4.
Repeat step 2 for each subsequent bit, working from the most significant to the least significant, until all 6 bits have been processed.

The resulting Gray code representation is obtained by combining the converted bits. The most significant Gray code bit (G5) corresponds to the most significant binary bit (B5), and so on.

Here's an example conversion using the above theory:

Let's say we have a 6-bit binary number: 101011.

To convert it to Gray code:

Start with the most significant bit:

B5 = 1, B4 = 0
XOR B5 and B4: 1 XOR 0 = 1
G5 = 1
Move to the next bit:

B3 = 1, B4 = 0
XOR B3 and B4: 1 XOR 0 = 1
G3 = 1
Repeat the process for the remaining bits:

B2 = 0, B3 = 1: XOR = 1, G2 = 1
B1 = 1, B2 = 0: XOR = 1, G1 = 1
B0 = 1, B1 = 1: XOR = 0, G0 = 0
So, the Gray code representation of the 6-bit binary number 101011 is 111100.

Please note that this theory assumes a basic understanding of binary arithmetic and logical operations such as XOR. The implementation of a 6-bit binary to Gray code converter can vary based on the specific hardware or programming language being used.
# LOGIC DIAGRAM
![image](https://github.com/arunkumarsukdevchavan/Simulation-project--Digital-Electronics/assets/118343978/85470d96-9916-413e-846e-155bc4d5bdcc)

# NETLIST DIAGRAM
![image](https://github.com/arunkumarsukdevchavan/Simulation-project--Digital-Electronics/assets/118343978/8b066da8-6688-485a-a730-21a0385dd7d6)

# TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/118678482/243264364-613de96b-8c60-4cf5-9f53-71e2c55014eb.png)
# PROGRAM
```
module sss (
input [5:0] binary,
output [5:0] gray
);
assign gray[5] = binary[5];
assign gray[4] = binary[5] ^ binary[4];
assign gray[3] = binary[4] ^ binary[3];
assign gray[2] = binary[3] ^ binary[2];
assign gray[1] = binary[2] ^ binary[1];
assign gray[0] = binary[1] ^ binary[0];
endmodule
```
# REFERENCE

https://github.com/arunkumarsukdevchavan/Simulation-project--Digital-Electronics/edit/main/README.md
