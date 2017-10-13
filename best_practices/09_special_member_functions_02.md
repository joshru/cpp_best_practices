### Special Member Functions cont.
- Special member functions all interact with each other. 
- Prefer to avoid defining member functions unless necessary.
- For example, defining a destructor will implicitly disables the generation of default move functions.
- Prefer to follow the [Rule of Zero](http://en.cppreference.com/w/cpp/language/rule_of_three) and never define any special functions unless your class must manage resources.
  - If managing resources, the special member functions should be defined with `=default` or `=delete` unless special behavior is needed.  