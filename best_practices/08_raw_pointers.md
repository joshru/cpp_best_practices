### Raw Pointers
- In interfaces, use raw pointers to denote individual obejcts (only) [(Core Guidelines)](http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rr-use-ptr)  

Terrible idea:
```c++
void print_ints(const int *s, int count) {
    for (int i = 0; i < count; ++i) {
        std::cout << s[i] << '\n';
    }
} 
int main() {
    const int ints[] = { 1,2,3,4,5 };
    print_ints(ints, 5);
}
```
Better idea: 
```c++
void print_ints(const vector<int> &t_ints) {
    for (const auto i : t_ints) {
        std::cout << i << '\n';
    }
} 
int main() {
    print_ints({ 1,2,3,4,5 });
}
```