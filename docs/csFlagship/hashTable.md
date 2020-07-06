# Class8 Hash Table $ String I

## Hash Table

- 逻辑层面的数据结构

1. `<key, value>` pairs, not allow **duplicate** keys
   - **fast search, insert/update, remove**

2. principle <key = string/int/obj..., value = obj,string,int...> e.g.,<string, int>

```ruby
Example:

    <tom,   1>
    <john,  2>
    <jerry, 5>
```


3. Hash table is a general data structure
    - HashMap and HashSet are its implementation classes in Java.

4. **syntax:**

```java
//java
HashMap<String, Integer> votes = new HashMap<String, Integer>();
...

int vote = votes.get(name);
vote++;
votes.put(name, vote);
```


```c++
//c++
std::unordered_map<String, int> votes;
votes[name]++;
```

- `ArrayList<Pair<String, Integer>>`

- get(key) - O(n)
- put(key, value) - O(n)



5. Implementation:
   - 5.1 hash collision
        - 5.1.1. chaining
        - 5.1.2. open address (probe + rehash)



