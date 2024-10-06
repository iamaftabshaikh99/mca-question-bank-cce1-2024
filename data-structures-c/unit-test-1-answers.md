
# Data Structures using C - Answers

## Unit Test 1 - October 2024

### Chapter 1:

1. **What is a Data Structure and explain their data types?**  
   **Short Answer**: A data structure is a way of organizing and storing data efficiently. Types include Primitive and Non-Primitive.
   
   **Detailed Answer**: 
   - **Primitive Data Structures**: These are basic structures such as `int`, `char`, `float`, and `bool`.  
   - **Non-Primitive Data Structures**: These include arrays, linked lists, stacks, queues, and graphs, which can handle more complex data.

   **Example**: Arrays store a fixed-size sequential collection of elements of the same type.

---

2. **What is Algorithm? Give one example.**  
   **Short Answer**: An algorithm is a step-by-step procedure for solving a problem.  

   **Detailed Answer**: An algorithm consists of input, a process, and output. It defines how a task is solved by following a specific series of steps.
   
   **Example**: Algorithm to find the largest number in an array:  
   1. Initialize `max` as the first element.  
   2. Traverse the array, comparing each element to `max`.  
   3. If an element is greater than `max`, update `max`.  
   4. Return `max`.

---

3. **What is Flowchart? Explain the symbols of a flowchart with any example.**  
   **Short Answer**: A flowchart is a graphical representation of an algorithm using symbols like oval (Start/End), rectangle (Process), and diamond (Decision).

   **Detailed Answer**: Flowcharts visually represent the sequence of operations in an algorithm.  
   **Common Symbols**:  
   - **Oval**: Start/End  
   - **Rectangle**: Process  
   - **Diamond**: Decision

   **Example**: A flowchart for checking if a number is even or odd involves inputting a number, checking `number % 2 == 0`, and then printing "Even" or "Odd".

---

4. **What is Algorithm? Explain its characteristics.**  
   **Short Answer**: An algorithm is a clear, finite, and effective sequence of instructions.  
   
   **Detailed Answer**: Characteristics of an algorithm include:  
   1. **Input**: It has one or more inputs.  
   2. **Output**: It produces at least one output.  
   3. **Definiteness**: Each step is well-defined.  
   4. **Finiteness**: It terminates after a finite number of steps.  
   5. **Effectiveness**: Each step must be basic enough to be carried out.

---

5. **What is Function? Give any example.**  
   **Short Answer**: A function is a block of code that performs a specific task.  

   **Detailed Answer**: Functions take inputs, process them, and return an output. They help in code reusability.

   **Example**: Function to calculate the sum of two numbers:  
   ```cpp
   int add(int a, int b) {
       return a + b;
   }
   ```

---

6. **What is Recursion? Give any example.**  
   **Short Answer**: Recursion is when a function calls itself to solve smaller instances of the same problem.  

   **Detailed Answer**: Recursion works by breaking a problem down into smaller, more manageable problems and using a base case to terminate the recursion.

   **Example**: Function to calculate factorial:  
   ```cpp
   int factorial(int n) {
       if (n == 0) return 1;
       else return n * factorial(n - 1);
   }
   ```

---

7. **Explain the complexity of an algorithm.**  
   **Short Answer**: Algorithm complexity refers to the time and space required to solve a problem.  

   **Detailed Answer**: The time complexity of an algorithm measures how fast it runs, and the space complexity measures how much memory it uses. Common notations include O(1), O(n), O(n^2), and O(log n).

   **Example**: Binary search has a time complexity of O(log n), making it more efficient than linear search (O(n)) for large datasets.

---

8. **What is the difference between static and dynamic memory allocation?**  
   **Short Answer**: Static memory allocation occurs at compile-time, while dynamic memory allocation occurs at runtime.

   **Detailed Answer**:  
   - **Static Memory Allocation**: Memory size is fixed during compile-time, e.g., `int arr[10]`.  
   - **Dynamic Memory Allocation**: Memory size is determined at runtime, e.g., using `malloc()` in C.

---

9. **What is an Array? How is the representation of an array done, and why is it required?**  
   **Short Answer**: An array is a collection of elements of the same type stored in contiguous memory locations.  

   **Detailed Answer**: Arrays are used to store multiple elements in one variable. They provide fast access via indexing.  
   **Example**: `int arr[5] = {1, 2, 3, 4, 5};`

---

### Chapter 2:

10. **What is Stack? Explain different operations used in stack (with example).**  
    **Short Answer**: A stack is a Last In First Out (LIFO) data structure.  
    
    **Detailed Answer**: Common stack operations include:  
    - **Push**: Add an element to the top.  
    - **Pop**: Remove the top element.  
    - **Peek**: View the top element.  
    - **isEmpty**: Check if the stack is empty.

    **Example**: Reversing a string using a stack involves pushing characters onto the stack and then popping them in reverse order.

---

11. **What is Stack? What are the various applications of stack?**  
    **Short Answer**: A stack is a LIFO data structure used in various applications like expression evaluation, function calls, and backtracking.

    **Detailed Answer**: Stack applications include:  
    - **Function calls**: Maintains the sequence of function calls.  
    - **Expression evaluation**: Evaluating postfix and prefix expressions.  
    - **Backtracking**: Solving mazes or puzzles.

---

12. **Write an algorithm to convert infix expression to postfix expression (with example).**  
    **Short Answer**: The Shunting Yard algorithm converts infix to postfix using a stack.

    **Detailed Answer**: 
    1. Traverse the infix expression.  
    2. If an operand, add to the output.  
    3. If an operator, push it to the stack after popping higher precedence operators to the output.  
    4. Pop the stack after the traversal is complete.

    **Example**: Infix: `A + B * C` → Postfix: `A B C * +`

---

13. **Write an algorithm for evaluation of postfix expression.**  
    **Short Answer**: Traverse the postfix expression, push operands to the stack, pop them when an operator is found, apply the operation, and push the result back.

    **Detailed Answer**: 
    1. Traverse the postfix expression.  
    2. If it's an operand, push it onto the stack.  
    3. When an operator is found, pop two elements, apply the operation, and push the result back onto the stack.

    **Example**: Postfix `2 3 * 5 +` evaluates to `11`.

---

18. **Write a program to calculate the area of a triangle using a function.**  
    **Short Answer**: Use the formula `0.5 * base * height` to calculate the area.  

    **Detailed Answer**: 
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
