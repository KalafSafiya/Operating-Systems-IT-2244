
This project contains two programs demonstrating process creation and execution using `fork()` in C. Both programs print numbers from 1 to 10, where:

- The **child process** prints numbers **1 to 5** and calculates their sum.
- The **parent process** prints numbers **6 to 10** and calculates their sum.

### Program Differences

- The **first program** uses separate loops and separate sum variables for the child and parent processes.
- The **second program** uses a single loop with a starting index determined by the process type, and a shared sum variable, making it more concise.

### Output

Both programs produce the same output with correct sums but may differ in the order of printed lines due to process scheduling.
