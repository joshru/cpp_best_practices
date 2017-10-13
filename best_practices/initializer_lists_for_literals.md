### Use Initializer Lists for Literal Values Only
- Attempting to use initializer lists for objects such as `std::shared_ptr` requires that expensive copies be created.   

Expensive example:
```c++
std::vector<std::shared_ptr<int>> vec{std::make_shared<int>(5)};
```