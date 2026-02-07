# OpenCPU
OpenCPU is an open source 4-bit processor digital circuit made in Logisim Evolution.

## Parts
- ALU (arithmetic logic unit)
- Half Adder
- Full Adder
- Control Unit (for instruction decoding)
- Final Register (to hold commands)
- WE_Auto_Enable (automatic write enable)
- Good Code

## Instructions
Currently, OpenCPU supports basic instructions using 1-bit or 4-bit commands:
- `0000` → ADD (adds ALU operands)
- `0001` → SUB (subtracts ALU operands)
- Additional instructions can be added using the 4-bit command system.

## Why I made it
I got bored ¯\_(ツ)_/¯  
But I also wanted to try out hardware development and see if I could build my own CPU.

## Notes
- This CPU is **not** production ready; it’s mostly a base start for anyone who wants to build their own CPU.
- The project is open source under the MIT License, so you can edit it and make it better.
- If you find any bugs or have suggestions, please open an issue.
- There is an OpenCPU_8B file that is a WIP 8 bit version of OpenCPU

## How it works
- ALU outputs feed into 1-bit registers (R0–R3) that store the results.
- A Control Unit decodes the register outputs into ALU operation selects and write-enable signals.
- A final 4-bit register holds the current command so the Control Unit can safely process it.
- WE_Auto_Enable ensures registers only latch results when a signal is present.
