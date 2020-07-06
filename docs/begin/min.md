# 539. Find Minimum

```
Given an array, return its minimum value

Example:

array = [7, 3, 2], return 2

Note: if the array is null or empty, return 0.
```


```java
public class Solution {
  public int min(int[] array) {
    // Write your solution here
    if(array == null || array.length == 0){
      return 0;
    }

    int min = array[0];
    for(int i = 0; i < array.length; i++){
      if(min > array[i]){
         min = array[i];
      }
    }
    return min;
  }
}
```

- note, if array[0] == null, and array's length is > 0, what happen?
- so we need to deal with corner case `if(array == null || array.length == 0){return 0}`