
# Types of Processor
---
## Von Neumann Architectures Flaws
![[von_neumann_architecture.png#invert_B|400]]
- Data and programs share the same memory. #Elaborate
- A program may overwrite data with programming instructions if not written carefully (e.g., [[Buffer Overflow]]).
- Programming instructions may be overwritten with data.
- Programming instructions and data share the same bus. This makes the processor slow as it waits for instructions.

## Harvard Architecture
![[harvard_architecture.png#invert_B|400]]
- Uses two separate memory spaces for program and data.
	- Two separate busses are used for transfer of program and data memory.

## Von Neumann vs Harvard Architecture
|                        | Von Neumann Architecture                                             | Harvard Architecture                                                                                 |
|------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Application            | PCs, servers and simple embedded systems.                            | Digital signal processing, image processing, audio processing in embedded systems.                   |
| Sharing in memory unit | Program memory and data memory share the same memory unit.           | Program memory and data memory are stored in separate memory units.                                  |
| Bus                    | A single bus is sued for transferring data and program instructions. | Program instructions and data are transferred via different busses which can be used simultaneously. |
| Program                | Optimized programs are used.                                         | Programs with larger memory requirements can be used.                                                |
## [[CISC]] vs [[RISC]]
|                                                        | Complex Instruction Set Computing (CISC)                                          | Reduced Instruction Set Computing (RISC)                                                                                    |
|--------------------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Architecture                                           | Intel or AMD                                                                      | ARM architecture                                                                                                            |
| Instructions                                           | Hundreds of instructions                                                          | Fewer instructions. Complex functions are performed by combining simple tasks                                               |
| Instruction cycle                                      | Complex instruction cycle. Instructions may have variable FDE cycles to complete. | Simple instruction cycle. Hence, RISC is more efficient at completing simple tasks.                                         |
| Speed                                                  | Typically built with higher clock speeds. Best suited for intensive tasks.        | RISC computers are often built with energy consumption in mind, and therefore, are built with lower clock speeds.           |
| Energy Consumption                                     | Larger CPUs, more energy consumption.                                             | Designed for lower energy consumption.                                                                                      |
| Design                                                 | Usually built with a cooling fan and heat sink.                                   | Typically, memory and other hardware are combined with the CPU on a single chip.                                            |
| Cost                                                   | More expensive.                                                                   | Less expensive.                                                                                                             |
| Examples                                               | Desktop and laptop computers.                                                     | Smart phones and tablets.                                                                                                   |
**Example of assembly instructions to perform a division on a CISC system**
```wasm

MOV AX, 3F4E

MOV BX, 4E

DIV BX

```

**Example of assembly instructions to perform a division on a RISC system**
```wasm

LXI H, 1040

MOV B, M

MVI C, 00

INX H

MOV A, M

CMP B

JC 3011

SUB B

INR C

JMP 3008

STA 2040

MOV A, C

STA 2041

HLT

```

## Co-processor Systems
#Todo 

## Parallel Processor Systems
There are four different types of parallel processor systems
- [[SISD]] (Single Instruction Single Data Stream)
- [[SIMD]] (Single Instruction Multiple Data Stream)
- [[MISD]] (Multiple Instruction Single Data Stream)
- [[MIMD]] (Multiple Instruction Multiple Data Stream)