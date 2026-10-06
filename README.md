C++ List STL – Basics
A beginner-friendly C++ program demonstrating the fundamental operations of the list container from the C++ Standard Template Library (STL).
📌 Overview
std::list is a doubly linked list provided by the C++ STL. Unlike a vector, elements in a list are not stored in contiguous memory. This allows efficient insertion and deletion at both the beginning and end of the list.
This program demonstrates:
- Creating a list
- Adding elements using push_back()
- Adding elements using emplace_back()
- Adding elements at the beginning using push_front()
- Using emplace_front()
- Common STL operations shared with vectors
✨ Features
- Demonstrates basic std::list operations.
- Shows insertion at both ends.
- Introduces push_back() and push_front().
- Demonstrates emplace_back() and emplace_front().
- Provides a foundation for understanding linked-list-based STL containers.
🛠️ Technologies Used
Technology	Purpose
C++	Programming language
STL	Standard Template Library
list	Doubly linked list container
iostream	Console input/output


📝 Problem Statement
Create a C++ program that demonstrates how to initialize and modify an STL list using different insertion operations.
Example Operations
Starting with an empty list:
{}

After:
ls.push_back(2);

The list becomes:
{2}

After:
ls.emplace_back(4);

The list becomes:
{2, 4}

After:
ls.push_front(5);

The list becomes:
{5, 2, 4}

🧠 Key Concepts
1. Creating a List
list<int> ls;

This creates an empty list capable of storing integers.
2. push_back()
Adds an element to the end of the list:
ls.push_back(2);

Result:
{2}

3. emplace_back()
Constructs and inserts an element directly at the end:
ls.emplace_back(4);

Result:
{2, 4}

4. push_front()
Adds an element to the beginning:
ls.push_front(5);

Result:
{5, 2, 4}

5. emplace_front()
Constructs an element directly at the beginning:
ls.emplace_front();

For int, this inserts a value-initialized element (0).
Note: The comment in the original code says {2, 4}, but emplace_front() on list<int> actually adds 0 to the front, producing {0, 5, 2, 4} based on the preceding operations.

🔄 Common List Operations
Several operations are also available for vectors and other STL containers:
begin()
end()
rbegin()
rend()
clear()
insert()
size()
swap()

However, the performance characteristics of these operations can differ between containers.
💻 Source Code
#include <iostream>
#include <list>
using namespace std;

void explainList() {
    list<int> ls;

    ls.push_back(2);       // {2}
    ls.emplace_back(4);    // {2, 4}

    ls.push_front(5);      // {5, 2, 4}

    ls.emplace_front();    // {0, 5, 2, 4}

    // Other commonly used functions:
    // begin, end, rbegin, rend,
    // clear, insert, size, swap
}

int main() {
    explainList();

    return 0;
}

▶️ How to Run
1. Compile the program
g++ main.cpp -o main

2. Run the executable
./main

Windows: Run main.exe instead.

📚 Learning Outcomes
This project helps beginners understand:
- STL list
- Doubly linked lists
- push_back()
- emplace_back()
- push_front()
- emplace_front()
- STL container operations
- Differences between linked lists and vectors
⏱️ Complexity
Operation	Complexity
push_back()	O(1)
emplace_back()	O(1)
push_front()	O(1)
emplace_front()	O(1)
Access by index	Not supported in O(1)
insert() at known position	O(1)
erase() at known position	O(1)
size()	O(1) in modern C++


A list is particularly useful when frequent insertions and deletions are required at known positions.
📸 Screenshot
Add your program output screenshot to:
screenshots/output.png

Then include it in the README:
![Program Output](screenshots/output.png)

Recommended project structure:
CPP-List-STL/
│
├── main.cpp
├── README.md
└── screenshots/
    └── output.png

👤 Author
Rishab Raj Chourasia
C++ | Data Structures & Algorithms | Problem Solving
