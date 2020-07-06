# 686. Remove duplicate element from array

```java
Given a 1D array and a known duplicate element (which appears more than once), 
remove the duplicate element and return the result array.

Input: array = [2, 3, 3, 4, 5], duplicate = 3
Output: [2, 4, 5]

Assume

(1) the input array is not null or empty 

(2) the duplicate element always exists in the input array and there is only one duplicate element.
```

```java
public class Solution {
  public int[] removeDuplicate(int[] array, int duplicate) {
    // Write your solution here
    int acc = 0;
    for(int i=0; i<array.length; i++){
      if(array[i] == duplicate){
        acc++;
      }
    }
    int [] tmp = new int [array.length - acc];
    int flag = 0;
    for(int j = 0; j<array.length; j++){
      if(array[j] == duplicate){
        continue;
      }
      tmp[flag++] = array[j];
    }
    
    return tmp;
  }
}

```