## 2.8 Supporting procedures in computer hardware

- **Procedure**: A stored subroutine that performs a specific task based on the parameters with 
  which it is provided.


- registers are the fastest place to hold data in a computer, so we want to use them as much as 
  possible. MIPS software follows the following convention for procedure calling in allocating its 
  32 registers:
  - **$a0 - $a3**: four argument registers in which to pass parameters
  - **$v0 - $v1**: two value registers in which to return values
  - **$ra**: one return address register to return to the point of origin












