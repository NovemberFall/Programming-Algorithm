# 552. Sum of Numbers in a Stack

```java
Calculate the sum of all numbers in a Stack.
Assumption: The Stack is not null or empty.


Example: 

Stack contains 7,5,3,0
Answer: 15
```



```java
class Solution {
	public int sumOfStack(Deque<Integer> stack) {
    int sum = 0;
    for(Integer x : stack){
      sum += x;
    }
    return sum;
	}
}
```





