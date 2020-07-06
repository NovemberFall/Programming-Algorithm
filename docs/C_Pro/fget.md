# fget()

- Declaration
- Following is the declaration for fgets() function.

```c
char *fgets(char *str, int n, FILE *stream)
```

- **stream** − This is the pointer to a FILE object that identifies the stream where 
  characters are read from.

- Because the operating system considers standard input like a file, 
  you can use `fgets()` to read text from the keyboard.

- Here’s a simplified version of the `fgets()` function as it applies to reading text input:
  - `fgets(string,size,stdin);`
  - In this example, `string` is the name of a char array, a string variable; 
    `size` is the amount of text to input plus one, which should be the same size 
    as the char array; and stdin is the name of the standard input device, 
    as defined in the stdio.h header file.

```c
#include <stdio.h>
int main()
{
  char name[10];
  printf("Who are you? ");
  fgets(name,10,stdin);
  printf("Glad to meet you, %s.n",name);
  return(0);
}
```