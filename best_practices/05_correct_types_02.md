### Correct Types cont.
 - Incorrect type comparison may incur unintended conversion overhead.
   - Can become an issue for algorithm correctness
 - Potential to incur unexpected behavior by limiting your range.
 - GCC can warn about type mismatch implicit conversions with the `-Wconversion` flag
 - Using `auto` for variables can often help avoid this issue entirely. 