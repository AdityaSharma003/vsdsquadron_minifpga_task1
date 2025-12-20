# Understanding Checks

## Q1. Where is the RISC-V program located in the vsd-riscv2 repository?

Ans1. The RISC-V reference program is located in the **`samples`** directory of the repository.

## Q2. How is the program compiled and loaded into memory?

Ans2. The program is translated from C into RISC-V machine code by the **`riscv64-unknown-elf-gcc`** compiler, and then the **Proxy Kernel (pk)** handles loading that code into the simulator's virtual memory so **`spike simulator`** can execute it.

## Q3. How does the RISC-V core access memory and memory-mapped IO?

Ans3. The RISC-V core uses Memory-Mapped I/O (MMIO) to access both RAM and peripherals by assigning each a unique address range on the system bus, allowing the processor to communicate with hardware using standard load and store instructions.

## Q4. Where would a new FPGA IP block logically integrate in this system?

Ans4. 
