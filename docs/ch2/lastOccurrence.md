# 16. Last Occurrence

```java
Given a target integer T and an integer array A sorted in ascending order, 
find the index of the last occurrence of T in A or return -1 if there is no such index

Assumptions
    - there can be duplicate elements in the array

Ex:
    - A = {1, 2, 3}, T = 2, return 1
    - A = {1, 2, 3}, T = 4, return -1
    - A = {1, 2, 2, 2, 3}, T = 2, return 3

Corner Cases
    - What if A is null or A of zero length? We should return -1 in this case
```



## Analysis

```java
target = 2;
Index:  0   1   2   3   4
Array:  1   2   2   2   3
Left:               1
Mid:                m
Right:                  r



target = 2;
Index:  0   1   2   3   4
Array:  1   2   2   2   2
Left:               1
Mid:                m
Right:                  r


[L, R] => it's guaranteed the last occurence of target has to be within L to R

array[mid] > target ? => [L, mid - 1] [L, mid] acceptable
array[mid] < target ? => [mid + 1, R] [mid, R] acceptable
array[mid] == target ?? => [mid, R]

=>

if(array[mid] <= target){
    //[mid, R]
    left = mid;
}else{
    right = mid - 1; //(right = mid)
}

Key points: V1.2
    * Think about how do you maintain the property(物理意义) of left, right
    * What should be the terminate condition?

```


```java
public class Solution {
  public int lastOccur(int[] array, int target) {
    // Write your solution here
    if(array == null || array.length == 0){
      return -1;
    }
    int left = 0;
    int right = array.length - 1;
    while(left < right - 1){
        int mid = (left + right) / 2;
        if(array[mid] <= target){
          left = mid;
        }else{
          right = mid;
        }
    }
    if(array[right] == target){
      return right;
    }else if(array[left] == target){
      return left;
    }
    return -1;
  }
}

```


```java
target = 3.2
1   3   5
        l
        m
        r
```