## Memory API | Address Space | Memory Leak

- 内存泄漏（Memory Leak）：内存泄漏是指在程序中动态分配的内存在使用后没有及时的释放掉而造成的系统无法再次使用

- [Memory API | Address Space | Memory Leak | Issue](https://github.com/NovemberFall/cs149_Operation-System/blob/master/class13_AddressSpace_MemoryAPI.md)

---

####  realloc()

- The C library function `void *realloc(void *ptr, size_t size)` attempts to resize the memory block 
  pointed to by `ptr` that was previously allocated with a call to `malloc` or `calloc`.

- Return Value
  - This function returns a pointer to the newly allocated memory, or NULL if the request fails.