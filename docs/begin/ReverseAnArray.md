# 542. Reverse an array

```
Given an array, reverse all its elements.

Example:

array = [2, 3, 5, 7, 11]

result: [11, 7, 5, 3, 2]

Assumption: The array is not null or empty.
```

- analysis:

```
[2   3    5    7   11]
 i->               <-j
     i->      <-j
          ij

i = 0;
j = array.length - 1;

1  <->  5
2  <->  4
3  <->  3
```


```java
public class reverse {
    public static void reverse(int[] array) {
        // Write your solution here
        if(array == null || array.length == 0){
            return;
        }
        int i = 0;
        int j = array.length - 1;
        while(i < j){
            swap(array, i, j);
            i++;
            j--;
        }
    }
    private static void swap(int[] array, int i, int j){
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }

    public static void main(String[] args) {
        int [] array = {2, 3, 5, 7, 11};
        reverse(array);
        for (int i : array) {
            System.out.print(i + " ");
        }
    }
}
```