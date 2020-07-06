# 544. Design an accumulator

```
Design an accumulator, which can take a new integer using function “add”, 
and can return the sum of all taken integers up to now using function “sum”.
```

```java
class Accumulator {
  private int acc;
	public void add(int x) {
    acc += x;
	}
	public int sum() {
    return acc;
	}
}
```