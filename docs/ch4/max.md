# 551. Maximum Number in a Queue

```java
Given a queue of integers, find the maximum number in it.

Assumption: the queue is not null or empty.


Example:

Queue contains 5,8,3,2,7
Answer: 8.
```

```java
class Solution {
	public int maxInQueue(Queue<Integer> queue) {
    int max = queue.poll();
    for(Integer x : queue){
      if(max < x){
        max = x;
      }
    }
    return max;
	}
}
```