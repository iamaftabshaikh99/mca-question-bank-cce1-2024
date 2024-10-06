
# Data Structures using C - Answers

## Unit Test 1 - October 2024

### Chapter 1:

1. **What is a Data Structure and explain their data types?**  
   A data structure is a way of organizing and storing data efficiently. There are two primary types:  
   - **Primitive**: Basic data types like `int`, `char`, `float`, and `bool`.  
   - **Non-Primitive**: More complex structures such as Arrays, Stacks, Queues, Linked Lists, Trees, and Graphs.  
   **Example**: Arrays store a fixed-size sequential collection of elements of the same type.

2. **What is Algorithm? Give one example.**  
   An algorithm is a step-by-step procedure to solve a problem.  
   **Example**: Algorithm to find the largest number in an array:  
   1. Initialize `max` as the first element of the array.  
   2. Traverse the array and compare each element with `max`.  
   3. If an element is greater than `max`, update `max`.  
   4. Return `max` after the loop ends.

3. **What is Flowchart? Explain the symbols of a flowchart with any example.**  
   A flowchart is a graphical representation of a process or algorithm using various symbols:  
   - **Oval**: Start/End.  
   - **Rectangle**: Represents a process or task.  
   - **Parallelogram**: Input/Output.  
   - **Diamond**: Decision points (Yes/No).  
   **Example**: Flowchart to check if a number is even or odd.

4. **What is Algorithm? Explain its characteristics.**  
   An algorithm is a well-defined procedure to solve a problem. Characteristics include:  
   1. **Input**: An algorithm has 0 or more inputs.  
   2. **Output**: An algorithm produces at least one output.  
   3. **Finiteness**: An algorithm terminates after a finite number of steps.  
   4. **Definiteness**: Each step is clearly defined.  
   5. **Effectiveness**: Each step can be carried out.

5. **What is Function? Give any example.**  
   A function is a block of code that performs a specific task. Functions can take input and return output.  
   **Example**: Function to calculate the sum of two numbers:  
   ```cpp
   int add(int a, int b) {
       return a + b;
   }
   ```

6. **What is Recursion? Give any example.**  
   Recursion is a method in which a function calls itself to solve smaller instances of the same problem until a base condition is met.  
   **Example**: Function to calculate the factorial of a number:  
   ```cpp
   int factorial(int n) {
       if (n == 0) return 1;
       else return n * factorial(n - 1);
   }
   ```

7. **Explain the complexity of an algorithm.**  
   The complexity of an algorithm refers to the time and space it requires to execute. It's often measured in terms of time complexity and space complexity. Common notations include:  
   - **O(1)**: Constant time.  
   - **O(n)**: Linear time.  
   - **O(n^2)**: Quadratic time.  
   - **O(log n)**: Logarithmic time.

8. **What is the difference between static and dynamic memory allocation?**  
   - **Static Memory Allocation**: Memory is allocated at compile-time, and its size is fixed.  
   - **Dynamic Memory Allocation**: Memory is allocated at runtime, and the size can change during program execution.

9. **What is an Array? How is the representation of an array done, and why is it required?**  
   An array is a collection of elements of the same type stored in contiguous memory locations. Arrays allow efficient access to elements using an index.  
   **Example**: In C++, `int arr[5] = {1, 2, 3, 4, 5};` is an array of size 5.

### Chapter 2:

10. **What is Stack? Explain different operations used in stack (with example).**  
    A stack is a linear data structure that follows the Last In First Out (LIFO) principle. Operations include:  
    - **Push**: Adds an element to the top of the stack.  
    - **Pop**: Removes the top element from the stack.  
    - **Peek**: Returns the top element without removing it.  
    - **isEmpty**: Checks if the stack is empty.  
    **Example**: Reversing a string using a stack by pushing each character and popping them in reverse order.

11. **What is Stack? What are the various applications of stack?**  
    A stack is used in:  
    - **Function calls**: Call stack maintains the sequence of function calls.  
    - **Expression evaluation**: Evaluating arithmetic expressions using postfix or prefix notation.  
    - **Backtracking algorithms**: Such as solving mazes or puzzles.

12. **Write an algorithm to convert infix expression to postfix expression (with example).**  
    **Algorithm**:  
    1. Initialize an empty stack and an output list.  
    2. Scan the infix expression from left to right.  
    3. If the scanned character is an operand, append it to the output list.  
    4. If it is an operator, push it onto the stack after popping higher precedence operators to the output.  
    5. Pop all operators from the stack after scanning.  
    **Example**: Infix `A + B * C` becomes Postfix `A B C * +`.

13. **Write an algorithm for evaluation of postfix expression.**  
    **Algorithm**:  
    1. Create an empty stack.  
    2. Traverse the postfix expression from left to right.  
    3. Push operands onto the stack.  
    4. When encountering an operator, pop the top two elements, apply the operator, and push the result back.  
    **Example**: Postfix `2 3 * 5 +` becomes (2 * 3) + 5 = 11.

14. **Convert the following expression from infix to postfix.**  
    (Provide specific examples as needed.)

15. **Convert the following expression from infix to prefix.**  
    (Provide specific examples as needed.)

16. **Evaluate the postfix expression.**  
    **Example**: Postfix `6 5 2 3 + 8 * + 3 + *` evaluates to `288`.

17. **Write an algorithm to convert a given infix expression to postfix expression.**  
    (Refer to question 12 for steps.)

18. **Write a program to calculate the area of a triangle using a function.**  
    **Example Code**:  
    ```cpp
    #include<iostream>
    using namespace std;

    float areaOfTriangle(float base, float height) {
        return 0.5 * base * height;
    }

    int main() {
        float base, height;
        cout << "Enter base and height: ";
        cin >> base >> height;
        cout << "Area of Triangle: " << areaOfTriangle(base, height) << endl;
        return 0;
    }
    ```

19. **Write a program to implement the addition of two polynomials using a one-dimensional and two-dimensional array.**  
    **Example**: Use arrays to store coefficients and degrees of the polynomials and add corresponding terms.

20. **Write a program to transpose a matrix.**  
    **Example Code**:  
    ```cpp
    #include<iostream>
    using namespace std;

    void transpose(int matrix[3][3], int transposed[3][3], int row, int col) {
        for (int i = 0; i < row; ++i) {
            for (int j = 0; j < col; ++j) {
                transposed[j][i] = matrix[i][j];
            }
        }
    }

    int main() {
        int matrix[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int transposed[3][3];
        transpose(matrix, transposed, 3, 3);

        cout << "Transposed Matrix:" << endl;
        for (int i = 0; i < 3; ++i) {
            for (int j = 0; j < 3; ++j) {
                cout << transposed[i][j] << " ";
            }
            cout << endl;
        }

        return 0;
    }
    ```

