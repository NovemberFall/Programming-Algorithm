# 635. Sum Of Squares

```
Problem: Give an array list of integer, calculate the sum of squares of all its elements.

Note: return 0 if the list is null or empty.

Example:

list = {1,2,3} → returns 14 
(14=1*1+2*2+3*3)
```

```java
public class Solution {
  public int sumOfSquare(List<Integer> list) {
        // Write your solution here
        if(list.isEmpty()){
            return 0;
        }
        Integer total = 0;
        for(Integer x : list){
            total += (x * x);
        }
        return total; 
  }
}
```