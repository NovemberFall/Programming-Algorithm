# 31. Queue By Two Stacks

```java
Java: Implement a queue by using two stacks. The queue should provide size(), isEmpty(), offer(),
poll() and peek() operations. When the queue is empty, poll() and peek() should return null.

C++: Implement a queue by using two stacks. The queue should provide size(), isEmpty(), push(), 
front() and pop() operations. When the queue is empty, front() should return -1.


Assumptions

The elements in the queue are all Integers.
size() should return the number of elements buffered in the queue.
isEmpty() should return true if there is no element buffered in the queue, false otherwise.
```

```java
public class Solution {  
  private Deque<Integer> in;
  private Deque<Integer> out;
  public Solution() {
    in = new LinkedList<>();
    out = new LinkedList<>();
  }
  
  private void shuffleIfNecessary(){
    if(out.isEmpty()){
      while(!in.isEmpty()){
        out.push(in.pop());
      }
    }
  }

  public Integer poll() {
    shuffleIfNecessary();
    return (out.isEmpty())? null : out.pop();
  }
  
  public void offer(int element) {
    in.push(element);
  }
  
  public Integer peek() {
      shuffleIfNecessary();
      if(out.isEmpty()){
        return null;
      }
      return out.peek();
  }
  
  public int size() {
    return in.size() + out.size();
  }
  
  public boolean isEmpty() {
    return in.isEmpty() && out.isEmpty();
  }
}
```

