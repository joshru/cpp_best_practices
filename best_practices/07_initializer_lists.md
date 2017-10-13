### Member Initializer Lists
- Prefer initializer lists for member variables.
  - Variables should be initialized in the order they are declared.
- Initializer lists **MUST** be used for `const` member variables.
- Consider using `std::move()` for values passed by reference. 