## C String | strdup

### How to convert integer to char in C ?

- To convert integer to char only 0 to 9 will be converted. 
  As we know 0's ASCII value is 48 so we have to add its value to the integer value to 
  convert it into the desired character hence

```c
int i = 5;
char c = i + '0';
```



- Just assign the `int` to a `char` variable.

```c
int i = 65;
char c = i;
printf("%c", c); //prints A
```
---

## strdup() 

- What is the purpose of the strdup() function in C?

- Exactly what it sounds like, assuming you're used to the abbreviated way in which C and 
  UNIX assigns words, it duplicates strings :-)
  - It tries to allocate enough memory to hold the old string 
    (plus a '\0' character to mark the end of the string).
    The `strdup()` function allocates sufficient memory for a copy of the string str, does the copy,
    and **returns a pointer to it**.
  - The pointer may subsequently be used as an argument to the function `free`
  - If insufficient memory is available, `NULL` is returned and `errno` is set to `ENOMEM`.


```c
char *strdup(const char *src) {
    char *dst = malloc(strlen (src) + 1);  // Space for length plus '\O'
    if (dst == NULL) return NULL;          // No memory
    strcpy(dst, src);                      // Copy the characters
    return dst;                            // Return the new string
}
```