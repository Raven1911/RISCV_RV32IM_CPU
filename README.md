# RISCV_RV32IM_CPU
* This is a RISC-V-RV32IM CPU(32 bit), support 5-stage pipelined, Hazard detection, Fowarding and basic instructions.
* System Clock up to 55 MHz (Depended on LUTs technology of FPGA Arty z7).
* The simulation and synthesised was done by Xilinx Vivado.

# Block Diagram
>![alt text](image/block_diagram.png)

# Instruction Types
>![alt text](image/InstructionType.png)
>
>
> Basic Instructions Supported:
> * and
> * or
> * add
> * sub
> * mul
> * addi
> * lw
> * sw
> * beq
