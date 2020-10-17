## 3.3 Multiplication

![](img/2020-10-16-14-58-43.png)

![](img/2020-10-16-15-07-55.png)

![](img/2020-10-16-15-20-07.png)

![](img/2020-10-16-15-20-24.png)

![](img/2020-10-17-09-43-54.png)

![](img/2020-10-17-09-44-12.png)

![](img/2020-10-17-09-48-29.png)

---

![](img/2020-10-17-10-14-31.png)

![](img/2020-10-17-12-04-14.png)

![](img/2020-10-17-12-07-48.png)


- Summary: Both MIPS multiply instructions ignore overflow, so it is up to the software to check to see 
  if the product is too big to fit in 32 bits. There is no overflow if <u>Hi is 0</u> for **multu** or 
  the replicated sign of Lo for **mult**. The instruction move from **hi (mfhi)** can be used to 
  transfer Hi to a general-purpose register to test for overflow.

![](img/2020-10-17-12-15-47.png)

---

![](img/2020-10-17-12-18-12.png)






























