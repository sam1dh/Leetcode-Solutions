<h1>Stack</h1>
    <p>
        Stack is a linear data structure that follows the <strong>LIFO</strong> (Last In First Out) principle. 
        The last element inserted is the first to be popped out. This means both insertion and deletion 
        operations happen at one end only.
    </p>
    <img src="1.png" alt="Stack visualization"width = 400; height: auto;">
 <h1>Basic Operations on Stack</h1>
    <p>
        In order to manipulate elements in a stack, there are certain operations provided to us:
    </p>
<h1>Basic Operations on Stack</h1>
    <p>
        In order to manipulate elements in a stack, there are certain operations provided to us:
    </p>
    <ul>
        <li><strong>push()</strong>: Inserts an element into the stack.</li>
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240606180844/Push-Operation-in-Stack-(1).webp" alt="Push Operation in Stack" width = 500; height: auto;">
        
<li><strong>pop()</strong>: Removes the top element from the stack.</li>
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240606180943/Pop-Operation-in-Stack-(1).webp" alt="Pop Operation in Stack" width = 500; height: auto;">
      <li><strong>top()</strong>: Returns the top element of the stack without removing it.</li>
      <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240606181023/Top-or-Peek-Operation-in-Stack-(1).webp" alt="Top or Peek Operation in Stack" width = 500; height: auto;">
        
<li><strong>isEmpty()</strong>: Returns <code>true</code> if the stack is empty; otherwise, returns <code>false</code>.</li>
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240606181101/isEmpty-Operation-in-Stack-(1).webp" alt="isEmpty Operation in Stack" width = 500; height: auto;">
        
  <li><strong>isFull()</strong>: Returns <code>true</code> if the stack is full; otherwise, returns <code>false</code>.</li>
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240606181147/isFull-Operation-in-Stack-(1).webp" alt="isFull Operation in Stack" width = 500; height: auto;">
    </ul>

<h2>
    Creation of Stack and Implementation of Stack.
</h2>
## Code Example

```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> st;

    // Push operation
    st.push(10); // Push 10 into the stack
    st.push(20); // Push 20 into the stack

    // Pop operation
    st.pop(); // Removes the top element (20)

    // Access the top element
    cout << "Top element is: " << st.top() << endl; // Output: 10

    // Check if the stack is empty
    if (st.empty()) {
        cout << "Stack is empty." << endl;
    } else {
        cout << "Stack is not empty." << endl;
    }

    return 0;
}

