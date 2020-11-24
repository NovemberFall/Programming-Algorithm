##  Introduction

- Principle of Locality (局部性原理，区域性原则)
  - Programs access a small proportion of their address space at any time 程序可随时访问其地址空间的一小部分
  - Temporal locality [计] 时间局部性
    - Items accessed recently are likely to be accessed again soon 最近访问的项目可能很快就会再次访问
    - e.g., instructions in a loop, induction variables
  - Spatial locality [计] 空间局部性
    - Items near those accessed recently are likely to be accessed soon 最近访问过的项目附近的项目可能很快就会被访问
    - E.g., sequential instruction access, array data 例如，顺序指令访问，数组数据
  
![](img/2020-11-23-22-15-21.png)


- **Temporal locality** 时间局部性: The locality principle stating that if a data location is referenced then it will tend to be referenced again soon.

- **Spatial locality** 空间局部性: The locality principle stating that if a data location is referenced, data locations with nearby addresses will tend to be referenced soon.

![](img/2020-11-23-23-01-42.png)  

---

- **Memory hierarchy** 分级存储器体系: A structure that uses multiple levels of memories; as the distance from the processor increases, the size of the memories and the access time both increase.













