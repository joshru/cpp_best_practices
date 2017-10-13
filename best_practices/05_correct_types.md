### Use Correct Types 
 - `unsigned` or `size_t` types should always be preferred when comparing against `size_t`  
 
For instance: 
```c++
    int main() {
        std::vector<int> v{1, 2, 3, 4};
        int sum = 0;
        for (int i = 0; i < v.size(); ++i) {
            sum += v[i]; // i is limited to ~2^31
        }
    }
```

Instead use:
```c++
    int main() {
        std::vector<int> v{1, 2, 3, 4};
        int sum = 0;
        for (unsigned i = 0; i < v.size(); ++i) {
            sum += v[i]; // i is limited to ~2^32
        }
    }
```
