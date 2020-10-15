## 3.2 Addition and subtraction

- **Arithmetic Logic Unit (ALU)**: Hardware that performs addition, subtraction, and usually 
  logical operations such as AND and OR.


![](img/2020-10-13-23-54-11.png)

![](img/2020-10-13-23-56-48.png)

![](img/2020-10-13-23-59-41.png)

![](img/2020-10-15-14-44-06.png)

![](img/2020-10-14-00-02-10.png)

---

- We have just seen how to detect overflow for two's complement numbers in a computer. What about 
  overflow with **unsigned integers**? Unsigned integers are commonly used for **memory addresses** 
  where overflows are ignored.


- The computer designer must therefore provide a way to ignore overflow in some cases and to recognize 
  it in others. The MIPS solution is to have two kinds of arithmetic instructions to recognize the two 
  choices:
  - Add (add), add immediate (addi), and subtract (sub) cause exceptions on overflow.
  - Add unsigned (addu), add immediate unsigned (addiu), and subtract unsigned (subu) **do not cause** 
    exceptions on overflow.


- Because C ignores overflows, the **MIPS C** compilers will always generate the unsigned versions of 
  the arithmetic instructions addu, addiu, and subu, no matter what the type of the variables. The MIPS 
  Fortran compilers, however, pick the appropriate arithmetic instructions, depending on the type of 
  the operands.


- A constant source of confusion for **addiu** is its name and what happens to its immediate field. The 
  **u** stands for unsigned, which means addition cannot cause an overflow exception. However, the 
  16-bit immediate field is sign extended to 32 bits, just like **addi, slti, and sltiu**. Thus, the 
  immediate field is signed, even if the operation is "unsigned."






























