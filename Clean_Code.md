# Principles of Clean Code
1. After making code work, spend time to make it clean.
2. Code must be intuitive for readers.
## Functions
### A function should do one thing
- To verify that your function does one thing, try to extract lines and create another function out of it.
- Too many well named functions are good for readability.
- Don't pass more than 3 arguments to a function.
- Don't pass true or false booleans in function.
- A well extracted function won't be more than 6 lines of code.
- Don't pass variable that stores output.

### Don't use switch statements
- Modifying a small thing needs modifications in switch statements each time.
- Better to use classes and define functions in it.
### Create functions to avoid side-effects
- Create a function that executes another function to avoid side-effects.
- Eg of side-effect is opening a file and forgetting to close it.
- To avoid forgetting to close a program, create function:
```c
void process_file(char *filename,     function processing_function){
    FILE *f = fopen(filename, "r");
    processing_function(f);
    free(filename);
}
```
- Differentiate between commands and queries.
### Have just try-catch block in function
- Try catch block should have just on function call.
- Never have nested try-catch statements.

