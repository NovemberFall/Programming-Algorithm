# 532. areRoughlyEqual

```
Check if the given number x and y are roughly equal, the allowed error is 0.0001.
```

- Instead of exact comparison with '==' you usually decide on some level of
  precision and ask if the numbers are "close enough":

```java
public class Solution {
  public boolean areEqual(double x, double y) {
    boolean b = (Math.abs(x - y) < 0.0001)? true : false;//complete the expression
    return b;
    // Write your solution here
  }
}
```