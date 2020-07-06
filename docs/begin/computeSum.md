# 540. Compute Sum

```
Given an array, return sum of all elements.

Example:

array = [7, 3, 2], return 12

Note: if the array is null or empty, return 0.
```



```java
public class Solution {
  public int sum(int[] array) {
    // Write your solution here
    if(array == null || array.length == 0){
      return 0;
    }

    int total=0;
    for(int i =0; i<array.length; i++){
      total += array[i];
    }
    return total; 
  }
}

```