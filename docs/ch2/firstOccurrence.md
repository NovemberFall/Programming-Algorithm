# 15. First Occurrence


```java
Given a target integer T and an integer array A sorted in ascending order, 
find the index of the first occurrence of T in A or return -1 if there is no such index.

Assumptions

There can be duplicate elements in the array.
Examples

A = {1, 2, 3}, T = 2, return 1
A = {1, 2, 3}, T = 4, return -1
A = {1, 2, 2, 2, 3}, T = 2, return 1

Corner Cases
What if A is null or A of zero length? We should return -1 in this case
```

## Analysis

```java
target: 2

Index:  0   1   2   3   4
Array:  1   2   2   2   3
        L
        M
            R



target: 3

Index:  0   1   2   3   4
Array:  1   2   2   2   3
                    L
                    M
                        R

while(L <= R)
[L, R] => if the target exists in the array, the first occurrence must be within [L, R]



jumps out of the loop condition: L == R - 1
target = 1;

Index:  0   1   2   3   4
Array:  1   2   2   2   3

Key points: V1.1
    * Think about how do you maintain the property(物理意义) of left, right
    * What should be the terminate condition?

```



```java
public class firstOccurrence {
    public static int firstOccur(int[]array, int target){
        if(array == null || array.length == 0){
            return -1;
        }
        int left = 0;
        int right = array.length - 1;

        //need to use left < right - 1 here to make sure there is no infinite loop
        //Think about the case when left == right - 1;
        //then mid == left, it will be possible picking [mid right] for next round
        //and it will go into an infinite loop in that case
        while(left < right - 1){ // l = r - 1, stop;
            //  0 element:
            //  1 element: can not jump out.
            //  2 element: left right   [2, 3], target = 3
            //              mid -> what if left = mid.
            //  3 element:  left    mid     right
            int mid = (left + right) / 2;
            if(array[mid] >= target){ //array[mid] >= target, 
                right = mid;
            }else{
                left = mid;
            }
        }
        
        //Make sure you understand all the possible situations when entering
        //this postprocessing procedure
        //1. array has only 1 element.
        //2. array has only 2 element.
        //3. left == right - 1 and left is the result
        //4. left == right - 1 and right is the result
        //5. left == right - 1 and none of left, right is the result

        //Post processing -> 1 element + 2 elements
        if(array[left] == target){
            return left;
        }
        if(array[right] == target){
            return right;
        }
        return -1;
    }

    public static void main(String[] args) {
        int[] A = {3, 4, 5, 6, 6, 9, 16};
        System.out.println(firstOccur(A, 6));
    }
}
```
---

```java
Time O(logN)
Space O(1)
```