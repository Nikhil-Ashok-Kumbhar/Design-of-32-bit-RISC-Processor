# Design-of-32-bit-RISC-Processor

1 Overview
The goal of this project is to design a 32-bit RISC microprocessor with load-store architecture with a 4-
stage pipeline and Harvard architecture. The project also includes the instruction and data memory
interfaces, register interface, and the entire pipeline control logic including full resolution of all structural,
control, and data hazards.
The memory interface will only support a single asynchronous memory interface.

2 Key Requirements
Here is a list of some key features based on the architecture developed in class.
- Harvard architecture constrained to one memory bus without cache until project 2
- 4-stage pipeline (IF, RR/ADDGEN, FO/EX, WB) as shown in class
- All instructions are 32-bits long as shown in class
- ALU operations involve only register values and short immediate values stored in the instruction
- The load/store instructions shall implement all modes shown in class
- Thirty-two 32-bit registers will be supported
- Stall-based structural hazard resolution for IF, FO, and WB memory access
- Data forwarding-based and stall-based hazard resolution for register operations
- Deferred flag resolution in WB for control hazard resolution (BRAcond)
- The memory space in provided with a single interface with A31..A2 + ~BE3..0 addressing
- You may assume that no data access crosses an aligned quad byte boundary
- Bank enable, bus control signals, and ready need to the implemented for memory interfaces
- Assume that all instructions are aligned to a quad byte boundary
- A register structure supporting multiple-simultaneous read/write operations needs to be implemented
- All operations in the class spreadsheet shall be supported
- No ALU internal design is required this semester
- Support for an external interrupt shall be provided with the vector read on the LSB of the data bus.
- The endian-ness of the processor must be chosen and clearly stated
- The SP pointer convention (post-/pre- inc/dec on push) must be chosen and clearly stated
