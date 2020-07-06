# 36. Middle Node Of Linked List

```
Find the middle node of a given linked list.

Examples

L = null, return null
L = 1 -> null, return 1
L = 1 -> 2 -> null, return 1
L = 1 -> 2 -> 3 -> null, return 2
L = 1 -> 2 -> 3 -> 4 -> null, return 2 

```

```java
look at this example:
L = 1 -> 2 -> 3 -> null, return 2

当 slow head, point to 1,  fast head point to 2
if only /*while(fast.next.next != null) */ condition, 
terminal condition is /* fast.next.next == null*/

for here, fast point to 2, fast.next.next == null, 也就是说 fast 在这里终止，不会再走下去，
所以必须改成 /* while(fast.next == null && fast.next.next != null) */
```



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
  public ListNode middleNode(ListNode head) {
    // Write your solution here
  }
}

```


- ans:

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
  public ListNode middleNode(ListNode head) {
    // Write your solution here
    if(head == null){
      return null;
    }
    ListNode slow = head;
    ListNode fast = head;
    while(fast.next != null && fast.next.next != null){
      slow = slow.next;
      fast = fast.next.next;
    }
    return slow;
  }
}
```