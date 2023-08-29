To use the 16-bit computer here are some things to note.
The first byte in any instruction is always the opcode.
The second byte contains information about what the CPU is supposed to do, and the next two bytes are usually an address.
Finally, the last two bytes are a word pointed to an address if the command is a write or read

  opcode   parameter        addr                                                            variable  
|0010 0101|0011 0000|0000 1000 1010 0110| 0x08a6 addr points to -> address in memory |0000 0000 0000 0110| 0x6

Hex code of the instruction:
25 03 08 a6 -> 00 06

What it's saying in plain English:
Read from address 08a6 and write the variable to register D.

The parameter byte can be divided into 4 sections, when doing an operation with a register the first 2 bits are not used the 2nd set of 2 bits are used for writing a specific register, the 3rd set of 2 bits are the B input which can be the 2nd input for a mathematical operation or a pointer to an address in memory, and the final set of 2 bits are the A input which is the 1st input for mathematical operations or a variable to be moved around.
