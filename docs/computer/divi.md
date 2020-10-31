## 3.4 Division

![](img/2020-10-17-12-26-29.png)

![](img/2020-10-17-12-38-44.png)

![](img/2020-10-17-12-40-08.png)

![](img/2020-10-17-12-41-23.png)

![](img/2020-10-17-12-57-00.png)

---

###  A divide algorithm.

- Using a 4-bit version of the algorithm to save pages, let's try dividing 7ten by 2ten, or 0000 
  0111two by 0010two.


- Answer:
  - The figure below shows the value of each register for each of the steps, with the quotient being 
    3ten and the remainder 1ten. Notice that the test in step 2 of whether the remainder is positive or 
    negative simply tests whether the sign bit of the Remainder register is a 0 or 1. The surprising 
    requirement of this algorithm is that it takes n + 1 steps to get the proper quotient and remainder.

![](img/2020-10-17-13-00-07.png)

![](img/2020-10-18-11-35-36.png)

![](img/2020-10-26-00-23-31.png)

![](img/2020-10-30-09-49-11.png)

---

![](img/2020-10-26-00-27-05.png)

![](img/2020-10-30-09-32-20.png)

---

### MIPS divide instructions ignore overflow 

- MIPS divide instructions ignore overflow, so software must determine whether the quotient is too 
  large. In addition to overflow, division can also result in an improper calculation: division by 0. 
  Some computers distinguish these two anomalous events. MIPS software must check the divisor to 
  discover division by 0 as well as overflow.

---

![](img/2020-10-30-20-48-46.png)

![](img/2020-10-30-20-56-02.png)



### Divide in MIPS

- The only requirement is a 64-bit register that can shift left or right and a 32-bit ALU that adds or 
  subtracts. Hence, MIPS uses the 32-bit Hi and 32-bit Lo registers for both multiply and divide.

- As we might expect from the algorithm above, `Hi` contains the remainder, and `Lo` contains the 
  quotient after the divide instruction completes.

- To handle both signed integers and unsigned integers, MIPS has two instructions: divide (div) and 
  divide unsigned (divu). The MIPS assembler allows divide instructions to specify three registers, 
  generating the mflo or mfhi instructions to place the desired result into a general-purpose register.


![](img/2020-10-30-20-59-47.png)


![](img/2020-10-30-21-08-41.png)


![](img/2020-10-31-08-18-18.png)

![](img/2020-10-31-08-18-33.png)

![](img/2020-10-31-08-19-42.png)


















