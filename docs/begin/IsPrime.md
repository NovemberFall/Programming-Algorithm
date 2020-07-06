# 535. Is Prime Number

```
Determine whether an integer n is a prime number. Assumption: n is >= 2.
```

- A simple solution is to iterate through all numbers from 2 to n-1 and for
  every number check if it divides n. If we find any number that divides, we return false.

```java
public class Solution {
  public boolean isPrime(int n) {
    // Write your solution here
    if(n <= 1){
      return false;
    }

    for(int i = 2; i<n; i++){
      if(n % i == 0){
        return false;
      }
    }
    return true;
  }
}

```