## flag

- Which flag is set when the result of a signed arithmetic operation(算术运算) is either too large or 
  too small to fit into the destination?
  - **Overflow** : is set when the result of an signed arithmetic operation is too large to fit in the 
    destination.



- zeor flag
  - the zero flag is quite simple if the result of the operation is a zero the zero flag will 
    be set otherwise it will be clear





## how to convert decimal to binary

- Write down the decimal number.
- Divide the number by 2.
- Write the result underneath.
- Write the remainder on the right hand side. This will be 0 or 1.
- Divide the result of the division by 2 and again write down the remainder.
- Continue dividing and writing down remainders until the result of the division is 0.
- The most significant bit (MSB) is at the bottom of the column of remainders and the least significant 
  bit (LSB) is at the top.
- Read the series of 1s and 0s on the right from the bottom up. This is the binary equivalent of the 
  decimal number.


![](img/2020-08-28-15-36-22.png)


![](img/2020-08-28-15-52-20.png)

- true

---

## how to convert decimal to Hexadeciaml

![](img/2020-08-29-18-09-24.png)

- e.g : Convert the number `1128` DECIMAL to HEXADECIMAL
  - step 1:  1128 / 16       result: 70           remainder(in hexadeciaml) : 8
  - step 2:  70 / 16       result: 4           remainder(in hexadeciaml) : 6
  - step 3:  4 / 16       result: 0           remainder(in hexadeciaml) : 4
  - so the final result: `468`

---

- another e.g.
  
![](img/2020-08-29-18-13-29.png)

- result: `1A6`


