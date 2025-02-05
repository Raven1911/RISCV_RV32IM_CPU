# RISCV_RV32IM_CPU
* This is a RISC-V-RV32IM CPU(32 bit), support 5-stage pipelined, Hazard detection, Fowarding and basic instructions.
* System Clock up to 55 MHz (Depended on LUTs technology of FPGA Arty z7).
* The simulation, synthesised and implementation was done by Xilinx Vivado.

# Block Diagram
>![alt text](image/block_diagram.png)

# Instruction Types
>![alt text](image/InstructionType.png)
>
>
> Basic Instructions Supported:
> * __and__
> * __or__
> * __add__
> * __sub__
> * __mul__
> * __addi__
> * __lw__
> * __sw__
> * __beq__

# I/O Port Configuration
>![alt text](image/RiscV32IM-IO.png)
> * __Input Ports__:
>   * __CLK__: System Clock.
>   * __Write_enable__: Enable saving of an value 8 bit instruction on the positive edge.
>   * __RST_n__: Reset system, Active low.
>   * __Sel_D/R__: If = 0, output value saved in DataMemory, else output value saved in register.
>   * __Instr_i__: Reads 8-bit instructions at a time on the positive edge of the Write_enable signal. It takes 4 positive edges of the Write_enable signal to read one instruction.
>   * __Addr__: Address that you want to access, this input is 5-bit since size of both DataMemory and Register are 32.
>   * __Value_o_addr__: The value saved in the memories are 32-bit, but our CPU can only ouput 8-bit at a time. Thus, we need to decide which 8-bit are to be read. For example, if value_o_addr = 0, the CPU will output the most signficant 8-bit in the address we assigned.
> * __Output Ports__:
>   * __value_o__ : Output value.