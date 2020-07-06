# argc

### What does argc mean?

- `argc` = `Arguement count`. This is used to determine the number of command line arguements 
  a program is run with.
- `argv` is called the argument vector which holds the names of all command line arguments including
  the name of your parogram.
- On any program you run, `argc` is always at least 1; and this is because the program itself is 
  included in the argument count. So in your program, argc is required to be 2 which consists of:
  `your_program` and `another_file`. if argc is not 2, this means it is equal to 1 or it is greater
  than 2 and since this is not what the program wants, the code aborts further execution.


- This should be covered in any tutorial for C++ (or C, ObjC, or related languages), 
  - [such as the GNU tutorial](http://crasseux.com/books/ctutorial/argc-and-argv.html)


- The `main` function of a C++ program has two parameters, by convention named `argc` and `argv`, 
  which give it the command-line arguments used to launch the program.

- `argc` is the count of arguments, and `argv` is an array of the strings.
  
- The program itself is the first argument, `argv[0]`, so `argc` is always at least 1.

- So, `argc` is 2 when the program is run with one command-line argument. 
  If it's run with no arguments, or more than one, the `argc != 2` will be true

---

- for exampe: `$ display_image firstarg "second arg"`

- The values will be:

```ruby
argc: 3
argv[0]: "display_image"
argv[1]: "firstarg"
argv[2]: "second arg"
```


---

## *argv[]  vs  **argv


- `char* argv[]` means array of char pointers, whereas `char** argv` means pointer to a 
  char pointer.

- In any array, the name of the array is a pointer to first element of the array, 
  that is, it contains the address of the first element.
  - so it is a pointer to another pointer