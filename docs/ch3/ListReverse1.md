# 34. Reverse Linked List (iterative)

```java
Reverse a singly-linked list iteratively.

Examples

L = null, return null
L = 1 -> null, return 1 -> null
L = 1 -> 2 -> 3 -> null, return 3 -> 2 -> 1 -> null
 
```

### my Analysis:

```java
ListNode prev, cur, next

Original Status:

prev    cur    next
        [1] -> [2] -> [3] -> null

*********************************************
start iteratively reverse:

        cur    next
prev <- [1]    [2] -> [3] -> null

        cur
       prev    next
     <- [1]    [2] -> [3] -> null


               cur
       prev    next
     <- [1]    [2] -> [3] -> null


               cur
       prev           next
     <- [1]    [2] -> [3] -> null


                      cur
              prev    next
     <- [1] <- [2]    [3] -> null


                      cur
              prev    next
     <- [1] <- [2] <- [3] -> null


                      cur
              prev           next
     <- [1] <- [2] <- [3] -> null


                      cur
                      prev   next
     <- [1] <- [2] <- [3] -> null



                             cur
                      prev   next
     <- [1] <- [2] <- [3] -> null
```

- code:

```java
/**
 * class ListNode {
 *   public int value;
 *   public ListNode next;
 *   public ListNode(int value) {
 *     this.value = value;
 *     next = null;
 *   }
 * }
 */
public class Solution {
  public ListNode reverse(ListNode head) {
    // Write your solution here
    ListNode prev = null;
    ListNode cur = null;
    ListNode next = null;
    cur = head;
    while(cur != null){
      next = cur.next;
      cur.next = prev;
      prev = cur;
      cur = next;
    }
    return prev;
  }
}

```










