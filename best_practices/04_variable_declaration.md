### Variable Declaration
- Never declare a variable until you have use for it. 
  - No group-creation of variables at the top of a function.
- Don't declare variables where they are unnecessary.  

  For example:
    ```c++ 
        const std::vector<std::string> numbers = {"1", "2", "3", "4"};
        for (const auto& number : numbers ) {
            std::cout << number << "\n";
        }
    ```  
    Becomes:
    ```c++ 
        // overall source and compiled size is reduced
        for (const auto& number : {"1", "2", "3", "4"} ) { 
            std::cout << number << "\n";
        }
    ```  