# 536. Calculate Sum of Squares

```
Meaning. Informally: When you multiply a whole number times itself, the resulting
 product is called a square number, or a perfect square or simply "a square." 
 So 1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, and so on, are all square
 numbers.
```

```
Calculate the sum of all square numbers between 1 and n (inclusive).

Example:


n = 3. Return 1;

n = 10. Return 14 (1 + 4 + 9);
```

```java
public class Solution {
  public int sumOfSquares(int n) {
    // Write your solution here
    int total = 0;
    for(int i = 1; i<= n; i++){
        if((i * i) <= n){
          total += (i * i);
        }
    }
    return total;
  }
}
```