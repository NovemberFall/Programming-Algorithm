# P9 Heap (PriorityQueue)

```ruby
min heap:

        1
       /  \
      3     5
     / \  
    6   4

index:  0    1   2   3   4
       [1,  3,  5,  6,  4] 




max heap:

         6
       /  \
      5     3
     / \  
    4   1

index: 0    1   2   3   4
      [6,   5,  3,  4,  1]
```


## PriorityQueue

- It is a **heap** with the same **Queue** interface with `offer()`, `peek()`, `poll()`
  But, it is not FIFO, when `poll()` or `peek()` we always look at the samllest/largest
  element (min heap/max heap)


- The PriorityQueue will arrange the elements based on the order of the elements 
  (who is smaller/larger by comparing any two of them) and it is optimized for problems
  about "who is the smallest/largest element".

- Internally it is implemented usign an array.

- **offer(E e)** - insert one element into the heap
- **peek()** - peek the top element in the heap (smallest/largest based on how to
  order the elements)
- **poll()** - remove the top element from the heap, and return it (smallest/largest
  based on how to order the elements)

- size()
- isEmpty()


- Time complexity:
  - offer(E e) - $$O(logn)$$
  - peek() - $$O(1)$$
  - poll() - $$O(logn)$$
  - remove() - throw exception vs poll - $$O(logn)$$, remove(Object) - $$O(n)$$
  - size() - $$O(1)$$
  - isEmpty() - $$O(1)$$

- Order - The PriorityQueue needs to know how to compare the elements and determine
  which one is smallest/larger.

---

## There are two ways to do so:

- <u>The element type implements Comparable Interface</u> 
  Example:

```java
PriorityQueue<Integer> minHeap = new PriorityQueue<Integer>();

minHeap.offer(4);
minHeap.offer(5);
minHeap.offer(2);
minHeap.offer(3);
minHeap.offer(1);

while(!minHeap.isEmpty()){
    System.out.println(minHeap.poll());
}


/* 
1
2
3
4
5
 */

```  

- How does the priorityqueue know how to compare the Integer objects?

- The element's class can implement Comparable interface and thus implement the
  required method compareTo(), PriorityQueue will use this method to compare any two
  elements.

```java
interface Comparable<E>{
    int compareTo(E ele);
}

public class Integer implements Comparable<Integer>{
    private int value;

    public Integer(int value){
        this.value = value;
    }

    @Override
    public int compareTo(Integer another){
        if(this.value == another.value){
            return 0;
        }
        return this.value < another.value ? -1 : 1;
    }

    public static void main(String[] args){
        Integer one = new Integer(1);
        System.out.println(one.compareTo(new Integer(5)));
    } // -1
}
```

- 1.compareTo(5) -> -1

- The return value of compareTo(another) method determines the order of this 
  another:
  - 0  - this and another are of the same priority
  - -1(<0) - this has higher priority than another
  - 1 (> 0) - this has less priority than another

---


### Another Example using custom class:

- Suppose you have an integer matrix, each row is sorted by ascending order and each
  column is also sorted by ascending order, we need a class to represent each cell in
  the maitrix, and we need to compare two cells with their value in the matirx.


```java
import java.util.PriorityQueue;
public class Cell implements Comparable<Cell>{
    public int row;
    public int col;
    public int value;

    public Cell(int row, int col, int value) {
        this.row = row;
        this.col = col;
        this.value = value;
    }

    @Override
    public int compareTo(Cell another){
        if(this.value == another.value){
            return 0;
        }
        return this.value < another.value ? -1 : 1;
    }

    public static void main(String[] args) {
        //we want to have a minHeap by the value of the Cell elements.
        PriorityQueue<Cell> minHeap = new PriorityQueue<>();
        Cell c1 = new Cell(0, 0, 0);
        Cell c2 = new Cell(0, 1, 2);
        int result = c1.compareTo(c2);
        System.out.println(result); // -1
    }
}
```