# Brewin# Interpreter
## Overview
The Brewin# Interpreter is an implementation of the Brewin# programming language. This language introduces need semantics, lazy evaluation, exception handling, and short-circuit evaluation for logical operators, building on the foundation of the original Brewin language.

## Key Features
### Need Semantics and Lazy Evaluation
- **Deferred Execution**: Expressions are only evaluated when their results are required.
- **Caching**: Once evaluated, results are stored for reuse, avoiding redundant computations.

### Exception Handling
- **Raise Statement**: Supports raising exceptions with custom messages.
- **Try/Catch Blocks**: Allows handling specific exceptions gracefully, propagating them as necessary.
- **Built-in Exceptions**: Automatically raises exceptions like division by zero.

### Short-Circuit Evaluation
- **Logical AND (&&)**: Skips evaluation of the second operand if the first is false.
- **Logical OR (||)**: Skips evaluation of the second operand if the first is true.

## Usage
### Prerequisites
- Python 3.11
- Ensure `intbase.py`, `brewparse.py`, and `brewlex.py` are in the project directory.

### Running the Interpreter
To run a Brewin program within `interpreterv1.py` or `interpreterv2.py`:
1. Create an instance of the Interpreter class.
2. Pass a Brewin program as a string to the run() method.
   For Example:
  ```
  def main():
    program = """
  func foo(a) {
    print("a: ", a);
    return a + 1;
  }
  
  func bar(b) {
    print(b);
  }
  
  func main() {
    var x;
    x = foo(5);
    bar(x);
  }
  
  /*
  *OUT*
  a: 5
  6
  *OUT*
  */
                  """
    interpreter = Interpreter()
    interpreter.run(program)
  
  
  if __name__ == "__main__":
      main()
  ```
## Test Cases
For running test cases, please refer to this repository: https://github.com/22sunm50/Brewin-Interpreter-Tests
