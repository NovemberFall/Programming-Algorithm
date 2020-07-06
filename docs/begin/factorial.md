# 537. Calculate Sum of Squares

```
求n的阶乘. Assumption, n > 1.

Example:


n = 3, return 6

n = 4, return 24

n = 5, return 120
```


```java
public class Solution {
  public int factorial(int n) {
    // Write your solution here
    if(n == 0){
      return 1;
    }else if(n == 1){
      return 1;
    }else{
      return n * factorial(n -1);
    }
  }
}
```
