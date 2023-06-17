# Week 1
### 1- What is the von Neumann Model/architecture?

Most computers use the stored program concept designed by mathematician John Von Neumann, which is a theoretical design describes the basic structure and functional units of a computer system. computers has five parts, an arithmetic-logic unit(ALU), control unit (CU), memory, input/output and system bus. 

Additions
- #### Types of Bus:
	- data bus -> read and write *usually used to classify microprocessors i.e, 16-bit microprocessors.*
	- address bus -> transmit registers addresses
	- control bus -> control the functions of other buses.

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

Addition:
RISC: SPARC (Scalar Processor Architechture)
