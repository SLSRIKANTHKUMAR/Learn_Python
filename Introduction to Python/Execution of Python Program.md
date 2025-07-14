# Python Execution Process with Diagram

Python is an interpreted language, which means the source code is executed line by line rather than being compiled all at once. Here's how Python code gets executed:

## Python Execution Flow

<img width="660" height="190" alt="image" src="https://github.com/user-attachments/assets/72ae89af-6872-45d3-909f-525c0d5500fc" />

```

## Step-by-Step Execution Process

1. **Source Code Creation**:
   - You write Python code in a `.py` file (e.g., `program.py`)

2. **Compilation to Bytecode**:
   - When you run the program (`python program.py`), Python first compiles the source code to bytecode
   - This bytecode is platform-independent and stored in `.pyc` files (cached for future use)
   - The Python compiler checks for syntax errors during this phase

3. **Bytecode Execution in PVM**:
   - The Python Virtual Machine (PVM) executes the bytecode line by line
   - The PVM is the runtime engine of Python that:
     - Loads the bytecode
     - Performs runtime checks
     - Handles memory management
     - Produces program output

4. **Runtime Behavior**:
   - During execution, Python:
     - Dynamically determines variable types
     - Checks for runtime errors (exceptions)
     - Manages memory automatically (garbage collection)

## Example Execution

Consider this simple program (`example.py`):

```python
def greet(name):
    return f"Hello, {name}!"

message = greet("Alice")
print(message)
```

Execution steps:
1. Compiler converts the source code to bytecode
2. PVM executes the bytecode:
   - Defines the `greet` function
   - Creates the `message` variable by calling `greet`
   - Executes the `print` function call
3. Output appears: `Hello, Alice!`

## Key Characteristics

- **Interpreted Nature**: No separate compilation step needed (unlike C/Java)
- **Dynamic Typing**: Type checking happens at runtime
- **Automatic Memory Management**: Garbage collector handles memory allocation/deallocation
- **Exception Handling**: Runtime errors are caught as exceptions

This execution model makes Python flexible and easy to work with, though it can be slower than compiled languages for some tasks.
