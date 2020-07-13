# ssize_t in C

- What is `ssize_t` in C?
  - In short, `ssize_t` is the same as `size_t` , but is a signed type - read `ssize_t` as 
    “signed size_t ”. `ssize_t` is able to represent the number -1 , which is returned by several system calls and library functions as a way to indicate error

- `ssize_t` is used for functions whose return value could either be a valid size, or a    
  negative value to indicate an error. It is guaranteed to be able to store values 
  at least in the range [-1, SSIZE_MAX] (SSIZE_MAX is system-dependent).

- So you should use `size_t` whenever you mean to return a size in bytes, 
  and `ssize_t` whenever you would return either a size in bytes or a (negative) error value.



# What is the size_t data type in C?

- It’s a type which is used to represent the size of objects in bytes and is therefore 
  used as the return type by the sizeof operator


