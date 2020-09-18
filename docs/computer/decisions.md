## 2.7 Instructions for making decisions

- **Conditional branch**: An instruction that requires the comparison of two values and that allows 
  for a subsequent transfer of control to a new address in the program based on the outcome of the 
  comparison.

- In contrast, an **unconditional branch** is an instruction that always follows the branch, as in 
  the "j" instruction in the animation below.


![](img/2020-09-18-09-54-49.png)

---

![](img/2020-09-18-09-56-51.png)

![](img/2020-09-18-09-57-18.png)

![](img/2020-09-18-09-57-47.png)

![](img/2020-09-18-10-01-34.png)

![](img/2020-09-18-10-03-03.png)

![](img/2020-09-18-10-03-50.png)

![](img/2020-09-18-10-04-27.png)

---

![](img/2020-09-18-10-14-39.png)

---

![](img/2020-09-18-10-18-36.png)

![](img/2020-09-18-10-19-49.png)

![](img/2020-09-18-10-24-06.png)

![](img/2020-09-18-10-30-18.png)

![](img/2020-09-18-10-35-13.png)

---

### Loops

![](img/2020-09-18-10-38-06.png)

![](img/2020-09-18-10-39-23.png)

![](img/2020-09-18-10-39-52.png)

![](img/2020-09-18-10-40-12.png)

---

![](img/2020-09-18-11-09-35.png)

![](img/2020-09-18-11-21-32.png)

---

###  More Conditional Operations

![](img/2020-09-18-11-25-46.png)

- The test for equality or inequality is probably the most popular test, but sometimes it is useful 
  to see if a variable is less than another variable. For example, a for loop may want to test to 
  see if the index variable is less than 0. Such comparisons are accomplished in MIPS assembly 
  language with an instruction that compares two registers and sets a third register to 1 if the 
  first is less than the second; otherwise, it is set to 0. The MIPS instruction is called set on 
  less than, or **slt**. For example, 
  - `slt  $t0, $s3, $s4   # $t0 = 1 if $s3 < $s4`

- means that register `$t0` is set to `1` if the value in register `$s3` is less than the value in 
  register `$s4`; otherwise, register `$t0` is set to `0`.
  Constant operands are popular in comparisons, so there is an immediate version of the set on less 
  than instruction. To test if register `$s2` is less than the constant `10`, we can just write
  - `slti $t0, $s2, 10    # $t0 = 1 if $s2 < 10`

