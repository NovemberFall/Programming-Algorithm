# Day2 ControlFlow and Methods

```java
public class Main {
    public static void main(String[] args) {
        int x = 11;
        if(x > 0){
            System.out.println("x>0");
        } else if (x > 5) {
            System.out.println("x>5");
        } else if (x > 10) {
            System.out.println("x>10");
        }else{
            System.out.println("others");
        }
    }
}

//output:  x>0
```

- the above only print: x>0; since the first statement if(boolean) is true
- it it print: x>0;   
- else if doesn't execute except if(boolean) return false

## EX 2

```java
    public static void main(String[] args) {
        int x = 11;
        if(x > 0){
            System.out.println("x>0");
        }

        if (x > 5) {
            System.out.println("x>5");
        }

        if (x > 10) {
            System.out.println("x>10");
        }

        System.out.println("others");

    }

/*  output:
x>0
x>5
x>10
others
 */
```


## in java, don't use:

```
if(1)
```

## for loop; 当你知道loop 次数时候用 for loop

## while loop; 当你不知道loop 次数的时候

---


## Break and Continue

1. Break: jumps out of the entire loop
2. Continue: skip the current iteration


```java
public class breakContinue {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5) {
                continue;
            }
            System.out.println(i + " ");
        }
    }
}

/* 
0 
1 
2 
3 
4 
6 
7 
8 
9 
 */
```

## break;

```java
public static void main(String[] args) {
    for (int i = 0; i < 10; i++) {
        if (i == 5) {
            break;
        }
         System.out.println(i + " ");
    }
}


/* 
0
1
2
3
4
 */
```

- more example:

```java
public class breakContinue {
    public static void main(String[] args) {
        int i;
        for (i = 0; i < 2; i++) {
            for (int j = 0; j < 5; j++) {
                if (j == 2) {
                    break;
                }
                System.out.println(i + "," + j + "");
            }
        }
    }
}

/* 
0,0
0,1
1,0
1,1
 */
```



## Function/method

- Complie error; 

```java
public class main {
    public static void main(String[] args) {
        int a = 11;
        int b = 6;
        int result = minFunction(a, b);
        System.out.println(result);
    }

    public static int minFunction(int n1, int n2) {
        return Math.min(n1, n2);
    }

    public static int minFunction(int n1, int n2) {
        return Math.min(n1, n2);
    }
}
```
