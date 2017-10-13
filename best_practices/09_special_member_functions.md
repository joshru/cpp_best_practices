### Special Member Functions
Special Functions:
``` c++
struct S {
    S();                    // default constructor
    S(const S&);            // copy constructor
    S(S&&);                 // move constructor
    S& operator=(const S&); // copy assignment
    S& operator=(S&&);      // move assignment
    ~S();                   // destructor
}
```