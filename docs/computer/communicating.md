## Communicating with people

![](img/2020-09-20-22-52-36.png)

![](img/2020-09-20-23-02-05.png)

---

- A series of instructions can extract a byte from a word, so load word and store word are 
  sufficient for transferring bytes as well as words. Because of the popularity of text in some 
  programs, however, MIPS provides instructions to move bytes. 
  - **Load byte `(lb)` loads a byte from memory, placing it in the rightmost 8 bits of a register**.
  - **Store byte `(sb)` takes a byte from the rightmost 8 bits of a register and writes it to memory.** 
  - Thus, we copy a byte with the sequence

```ruby
lb $t0, 0($sp)   # Read byte from source
sb $t0, 0($gp)   # Write byte to destination
```


