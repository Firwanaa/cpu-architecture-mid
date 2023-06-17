# Week 1
### 1- What is the von Neumann Model/architecture?

Most computers use the stored program concept designed by mathematician John Von Neumann, which is a theoretical design describes the basic structure and functional units of a computer system. computers has five parts, an arithmetic-logic unit(ALU), control unit (CU), memory, input/output and system bus. 


### 2- When was the Von Neumann architecture invented?
1946

### 3- Has the Von Neumann Architecture been changed till recently?
The architecture still wildly used, very few use the pure model, most computers add another step to check for interrupts, electronic events that could occur any time.
it has seen many advancements such as pipelining, the introduction of RISC, parallel processing, power optimisation and many other things to improve performance and efficiency. Even though quantum computing is introduced recently it's still limited to lab use and still not production ready. 

### 4- Which computers are made from The von Neumann Model? 
The majority of computers like PC, laptops and mobile phones are based on Von Neumann model. Most intel and AMD processors are based on Von Neumann, but very few used the pure model. 

### 5- Provide the actions that a Von Newmann computer emulate.

- **instruction fetch**: obtain instructions from storage
- **instruction decode**: determine required actions and instruction size.
- **operand fetch**: locate and obtain operand data.
- **execute**: compute results 
- **result store**: deposit result into storage for later use
- **next instruction**: determine successor instruction

# Week 2:
### 1- Provide the main components of a CPU.
- **ALU**: Arithmetic logical unit: performs arithmetic and logical operations. 
- **IR**: Instruction Register: used to store the copy of currently used instruction
- **PC**: Program counter: contains the address of instruction currently used.
- **SP**: Stack pointer: contains address of the 'top' the stack
- **PS**: Processor status register: contains condition code which allow conditional jump
- **MAR**:Memory Address Register: contains the address of the memory location (RAM) to read/write
- **MBR***: Memory Buffer Register: contains data to be read/write form/to a memory location. 
- **DR**: Data Registers: storage places inside CPU where access is much faster than accessing RAM
- **XR**: Index Register: Used with high-level programming languages that use arrays.

### 2- Provide register names for Program counter in Intel/ARM processors.
In intel processor it's called **Instruction Pointer IP**.
In ARM processor it's called **Program Counter PC**.

### 3- Provide register names for storing Processor states in Intel/ARM processors?
In Intel processors knows as Flag Registers:
	- CF: carry flag
	- ZF: zero flag
	- SF: sign flag
	- OF: overflow flag

In ARM known as Program Status Registers **PSR**:
	- N: Negative
	- Z: Zero
	- C: Carry
	- V: Overflow

### 4- Provide register names for storing the top of the Stack in Intel/ARM processors:
In Intel and ARM is called: **Stack Pointer SP**

### 5- Describe the general differences between CISC and RISC computers
- CISC (complex instruction set computer), larger number of instructions, usually 200-300, each CISC instruction can be broken down into smaller cycles to complete.
- RISC (reduced instruction set computer): smaller number (around 50) of simple instructions that execute in one cycle each. 

|   |   |   |
|---|---|---|
||CISC|RISC|
|Instruction Set <br><br>(# of instructions)|200-300|Less than CISC About 50|
|CPI|broken down to a<br><br>number of microinstructions<br><br>Require one or more|fewer cycles 1|
|Is the Length of instruction is fixed?<br><br>(# of byte / instruction)|16 bit|vary|
|Register set<br><br> (# of registers)|14 registers (emu8086)|32 or more|
|Memory access instructions<br><br> (# of instruction for memory access)|Load and store<br><br>memory-to-memory|Load and store <br><br>memory -to- register<br><br>register-to-memory|
|Suitable for parallel processing|Less suitable due to more complex instructions|Yes, by using pipelining|
|Are Micro Instructions required|Yes (more complex)|No (simpler)|


### 6- Provide the names of the computer implemented the CISC architecture...
Intel (intel 8086) and IBM mainframes

### 7- Provide the names of the computer implemented the RISC architecture...
RISC: SPARC (Scalar Processor Architecture) which was evolved form the MIPS (Microprocessor without Interlock Pipeline stages)

### 8- How many bits in a byte?
1 Byte = 8 bits
word = 32 bits (4 bytes) <- depends on the Architecture

### 9- How many sub buses are there in the bus system of our processor?

- #### Types of Bus:
	- data bus -> read and write *usually used to classify microprocessors i.e, 16-bit microprocessors.*
	- address bus -> transmit registers addresses
	- control bus -> control the functions of other buses.
 
### 10- How many instructions in EMU8086?
116 instructions (not sure if it's 116 or 117)

### 11-What is a combinational logic?

### 12- List the characteristics of a RISC computer.
- smaller number of instructions: about 50
- simple instructions that execute in one cycle each (opposed to CISC need to be broken into micro code which require more cycles)
- RISC instructions are not interpreted
- Power efficiency 

### 13- Provide the data range ( max – min) of a 2-byte variable, 4 byte variable.
##### 2- byte
- signed: -32,768 to 32,767
- unsigned: 0 to 65,535

##### 4- byte
- signed: -2,147,483,648 to 2,147,483,647
- unsigned: 0 to 65,535

```
it can be done without memorization:
- unsigned 2-byte:
1 byte = 8 bits
2 bytes = 16 bits
2^16 = 65,536
starting from 0, therefore range: 0 - 65,535
- unsigned 4-byte:
4 bytes = 32 bits
2^32 = 4,294,967,295
starting from 0, therefore range: 0 - 4,294,967,294

- signed 2-byte:
- 2 bytes = 16 bits
- 1 bit reserved for sign: we left with 15 bits
- range is (-2^15 to 2^15 - 1) = -32,768 to 32,767

- signed 4-byte:
- 4 bytes = 32 bits
- 1 bit reserved for sign: we left with 31 bits
- range is (-2^31 to 2^31 - 1) = -2,147,483,648 to 2,147,483,647

** notes:
only need to know number of bits
signed: 2^(# of bits) and then subtract 1 since we start from 0
unsigned: 1 bit is for the sign (+-), -2^(# of bits) to 2^(# of bits) - 1
```


### 14- The data word is stored in memory as below:
Memory Addr.: value in this memory cell:
60012 18
60013 2C
60014 7F
60015 39


### What is the value represented by “Big-Endian” format and what is the value represented by “Little-Endian” format when a CPU reads the word?

- Big-Endian: 

| 60012 | 60013 | 60014 | 60015 |
|-------|-------|-------|-------|
| 18    | 2C    | 7F    | 39    |


- Little-Endian:

| 60012 | 60013 | 60014 | 60015 |
|-------|-------|-------|-------|
| 39    | 7F    | 2C    | 18   |



### 15 - An integer data in the cpu is: A1 B2 C3 D4, We want to store the data on memory, how is this data stored in memory when using Little-Endian? how is this data stored when using Big-Endian?

- Big-Endian:    A1 B2 C3 D4 (A1 is stored in the MSB)
- Little-Endian: D4 C3 B2 A1 (A1 is stored in the LSB)

### 16- A compiler designer is trying to decide between two code sequences for a particular machine. The hardware designers have supplied the following facts: For a particular high-level language, the compiler writer is considering two sequences that require the following instruction counts: What is the CPI for each sequence? Which code sequence is faster ?
![[Pasted image 20230617143733.png]] 

$CPIa = \dfrac{6\times2 + 7\times 5 + 5\times 6}{6+7+5} =4.2$


$CPIb = \dfrac{3\times2 + 8\times 5 + 2\times 6}{6+7+5}=4.4$

> CPIb is faster

