# RVI

This project mainly aims to design assembler for  RV32I instruction set. The assembler aims to allow for selectively turning off instruction and easily modify instruction opcodes.It accounts This project mainly aims to design assembler for  RV32I instruction set. The assembler aims to allow for selectively turning off instruction and easily modify instruction opcodes. It accounts for 37 instructions and is designed to work for python assembly code.
An assembler is system software which is used to convert an assembly language program to
its equivalent object code. The input to the assembler is a source code written in assembly
language (using mnemonics) and the output is the object code. The design of an
assembler depends upon the machine architecture as the language used is mnemonic
language.


## Supported Instructions

|Sl. No| I Type| R Type | U Type | UJ Type| S Type| SB Type|
|------|-------|--------|--------|--------|-------|--------|
|1     |addi   |add     |lui     |jal     |sw     |beq     |
|2     |slti   |sub     |auipc   |        |sb     |bne     |
|3     |sltiu  |sll     |        |        |sh     |blt     |
|4     |ori    |slt     |        |        |       |bltu    |
|5     |xori   |sltu    |        |        |       |bge     |
|6     |andi   |xor     |        |        |       |bgeu    |
|7     |slli   |srl     |        |        |       |        |
|8     |srli   |sra     |        |        |       |        |
|9     |srai   |or      |        |        |       |        |
|10    |jalr   |and     |        |        |       |        |
|11    |lw     |        |        |        |       |        |
|12    |lb     |        |        |        |       |        |
|13    |lh     |        |        |        |       |        |
|14    |lbu    |        |        |        |       |        |
|15    |lhu    |        |        |        |       |        |


## Installation

#### Step 1:
The assembler works on `Python3`. Plese create a `python3` virtualenvironment
in your system. For linux systems with `virtualenv` installed, this is as
simple as running
```
virtualenv -p python3 bcd
```

This creates a new virtual environment named `bcd`. For Windows, Anaconda, or
other environments, plese refer to your environment specifc instructions.
 
#### Step 2:

*After activating* the environment created in step 1, install the requirements

    pip3 install ply==3.9 

## Usage

In the simplest case, the usage is as follows. `cd` to the `src/`
directory. To assemble a input file `fib.bcd`, type

    $  python3 bcd.py fib.bcd -o fib

where the `bcd` extension has no special meaning, and any type of file will
actually do.




