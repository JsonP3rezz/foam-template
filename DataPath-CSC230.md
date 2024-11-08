# DataPath
Implementation of MIPS instruction datapath through the MIPS processor

# Core MIPS Instructions 

#### Core MIPS instructions, include but are not limited to:
  
  - Memeory reference Intructions `lw` and `sw`.
  - arithmetic-logical instructions `add`, `sub`, `and`, `or`, and `slt`
  - instructions branch equal `beq` and jump `j`

#### For every instruction, the first two steps are identical

1. [[IF stage]] - Send the [[program counter]](PC) to the memory that contains the code and fetch the instruction from that memory.
   
2. [[ID stage]] - Read one or two registers, using fields of the instruction to select the registers to read. For the load word instruction, we need to read only one register, but most other instructions require reading two registers.

#### [[EX stage]] - Most instructions will use the [[ALU]]  

with the execption of jump instructions, the data path and flow of many instructions will incorperate the [[ALU]].

- Memory Reference Instructrions - ALU for [[address calculation]].
- Arithmatic-Logic Instructions - ALU for [[operation execution]]
- Branch Instructions - ALU for [[comparisons]] 
  
