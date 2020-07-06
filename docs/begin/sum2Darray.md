# 543. Sum of 2D array

```
Given a two-dimensional array, calculate the sum of all its elements

Example:

array = {{ 2, 3}, {4, 5}, {1, 0}}

Return 15

Assumption: The 2D array is not null or empty. The 2D array is rectangular
shape.
```


```java
public class Solution {
  public int sum(int[][] array) {
    // Write your solution here
    int total = 0;
    for(int i = 0; i<array.length; i++){
      for(int j=0; j<array[0].length; j++){
        total += array[i][j];
      }
    }
    return total;
  }
}
```