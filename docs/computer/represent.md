## 2.5 Representing instructions in the computer

![](img/2020-09-17-14-14-39.png)

![](img/2020-09-17-14-16-03.png)

![](img/2020-09-17-14-17-31.png)

![](img/2020-09-17-14-19-37.png)

![](img/2020-09-17-14-21-48.png)

![](img/2020-09-17-14-23-29.png)


- This layout of the instruction is called the `instruction format`. As you can see from counting 
  the number of bits, this MIPS instruction takes exactly 32 bits—the same size as a data word. In 
  keeping with our design principle that simplicity favors regularity, 
  **all MIPS instructions are 32 bits long**.

![](img/2020-09-17-14-30-27.png)

![](img/2020-09-17-14-57-22.png)

---

![](img/2020-09-17-14-33-37.png)

![](img/2020-09-17-14-39-11.png)

---

#### Hexadeciaml: Number in base 16

![](img/2020-09-17-14-42-14.png)

![](img/2020-09-17-14-45-17.png)

![](img/2020-09-17-14-46-49.png)


---

### A second type of instruction format is called I-type

![](img/2020-09-17-15-00-19.png)

- The 16-bit address means a load word instruction can load any word within a region of ±2^15 or 
  32,768 bytes (±2^13 or 8192 words) of the address in the base register rs. Similarly, add 
  immediate is limited to constants no larger than ±2^15. We see that more than 32 registers would 
  be difficult in this format, as the rs and rt fields would each need another bit, making it harder 
  to fit everything in one word.


![](img/2020-09-17-16-04-18.png)



![](img/2020-09-17-16-05-39.png)

![](img/2020-09-17-16-06-18.png)

![](img/2020-09-17-16-08-06.png)

![](img/2020-09-17-17-40-00.png)

![](img/2020-09-17-17-53-03.png)

![](img/2020-09-17-18-05-02.png)

![](img/2020-09-17-18-14-02.png)

- Note: `35` represents `opecode` for `lw` in `Decimal` 
- Note: `43` represents `opecode` for `sw` in `Decimal` 

---

### Example 2.5.2: Translating MIPS assembly language into machine language.

![](img/2020-09-17-18-45-35.png)

![](img/2020-09-17-18-51-58.png)

![](img/2020-09-17-19-27-32.png)

---

![](img/2020-09-17-19-35-10.png)

![](img/2020-09-17-19-35-52.png)

![](img/2020-09-17-19-41-34.png)

---


### The Big Picture

![](img/2020-09-17-19-44-49.png)

![](img/2020-09-17-19-49-52.png)

![](img/2020-09-17-19-50-22.png)

![](img/2020-09-17-19-54-37.png)





