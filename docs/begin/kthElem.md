# 561. Find the Kth Element in The Matrix

```java
Given a matrix, find the Kth index element.

example: 

matrix:

1 3 4

5 6 7

8 9 10

k = 4 → return: 6
```


```java
public class Solution {
  public int findElement(int[][] matrix, int k) {
    // Write your solution here
    int m = matrix.length;
    int n = matrix[0].length;
    return matrix[k/n][k%n];
  }
}

```