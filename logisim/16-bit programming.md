To use the 16-bit computer here are some things to note.
The first byte in any instruction is always the opcode.
The second byte contains some information of what the CPU is suppose to do, and the next two bytes are usally an address.
Finally, the last two bytes are a word pointed to an address if the command is a write or read

  opcode   parameter        addr                                                            variable
  
|0010 0101|0011 0000|0000 1000 1010 0110| 0x08a6 addr points to -> address in memory |0000 0000 0000 0110| 0x6

Hex code of the instruction:
25 03 08 a6 -> 00 06

What it's saying in plain english:
Read from address 08a6 and write the variable to register D.
