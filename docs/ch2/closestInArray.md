# 17. Closest In Sorted Array

```java
Given a target integer T and an integer array A sorted in ascending order, 
find the index i in A such that A[i] is closest to T.

Assumptions:
    - There can be duplicate elements in the array, 
    and we can return any of the indices with same value.


Examples:

A = {1, 2, 3}, T = 2, return 1
A = {1, 4, 6}, T = 3, return 1
A = {1, 4, 6}, T = 5, return 1 or 2
A = {1, 3, 3, 4}, T = 2, return 0 or 1 or 2


Corner Cases:

What if A is null or A is of zero length? We should return -1 in this case.
```


## Analysis:

```java
target = 2, 6

    0   1   2   3   4   5
   [1,  3,  4,  5,  5,  7]
                    L
                    M
                        R
   
   [L, R]: The closest element to target must be in [L, R]

    Key points: V1.1
        * Think about how do you maintain the property(物理意义) of left, right
        * What should be the terminate condition?

```


```java
public class Solution {
  public int closest(int[] array, int target) {
    // Write your solution here
    if(array == null || array.length == 0){
      return -1;
    }

    int left = 0;
    int right = array.length - 1;

    //key point 1 -- target exists in the [left, right]
    //key point 2 -- jump out of the while loop normally
    while(left < right - 1){
      int mid = (left + right) / 2;
      if(array[mid] == target){
        return mid;
      }else if(array[mid] > target){
        right = mid;
      }else{
        left = mid;
      }
    }
    
    //post processing
    if(Math.abs(array[left] - target) <= Math.abs(array[right] - target)){
      return left;
    }
    return right;
  }
}
```

---


```java
Time O(logn)
Space O(1)
```