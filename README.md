02_Cpp
======

Intro to C++, learning to do things you can already do in Java

Reading
=======

**C++ Programming** at WikiBooks.

All of the readings are free online, though note that the book is under constant revision. If something looks crazy, ask me about it.

I will lecture about this material in class. These readings are meant to be used in reviewing/studying.

1. Why our code is split into .h files and .cpp files: https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/File_Organization (6p)
2. What is the :: operator for? https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Scope Stop at "unnamed namespace"
3. What does the compiler do? What does it NOT do? What does the pre-processor do? What does the linker do? https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler Stop at "Compile speed" (4p) https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler/Preprocessor (13p) https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler/Linker (4p)
4. Bitwise operators. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Bitwise_operators (2p)
5. Arrays, and the subscript operator. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Subscript_operator_.5B_.5D (5p)
6. Pointers. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#address-of_operator_.26 and https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Pointers.2C_Operator_.2A (9p) Skip the part about multi-dimensional arrays, and the part about pointers to functions.
7. Dynamic memory allocation. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Dynamic_memory_allocation (4p)

Homework
========

1. Fork this repo
3. Fill in the blanks in the main.cpp with code that produces the correct result. Read the comments to find out what they ought to do.
4. Be sure to `git commit` and `git push` often
5. Update this file with your documentation and the answers to questions.
6. When you are ready to turn in your homework, submit a pull request from your repo to mine.
7. Be sure to check the pull requests for my repo on github to make sure it worked, and that your work has been submitted.

Documentation
=========

For each of the following functions in main.cpp, tell me whether or not you think it is working in your submission.

1. prime - Working
2. defix - Working
3. sumSlice - Working
4. square - Not working. Could not figure out how to make it look like in the description. Will finish it during the week as I had to delete most of my code, I was using std::cout wrong and had a giant wall of if statements that made no sense. 
5. listPrimes - Working

Questions
=======

#### 1. In C++, the compiler compiles each .cpp file separately, without looking at the others. Explain why this leads to the need for .h files.
Without .h or header files, one must declare each method and class used above main. This leads to a huge wall of text that must be put in each .cpp file. With header files, one can simply declare each method in a separate file then tell the preprocessor to look in that file for each methods declaration. This makes files much easier to read, improves compilation speed, and increases organization.

#### 2. Explain the individual roles of the preprocessor, the compiler, and the linker. What type of inputs do they take? What kind of outputs do they produce? What is the purpose of each?
The preprocessor accepts changes to the source code and alters the way it will be compiled. The preprocessor accepts any directive that starts with #. The compiler translates source code into object files that contain machine code. The linker accepts object files created by the compiler and translates them into an executable file. 

#### 3. What is a "pointer"?
A pointer is a stored memory address that "points" to another memory location on the computer. A null pointer is a special type of pointer that doesn't point to anything. A pointer can be assigned by adding a *

#### 4. If I have a variable declared as `int x`, how do I find out what memory address that variable is stored at?
To find the memory address of a variable you place an & before the variable then assign that to something. To get the memory address of int x, we print out &x or store &x in a pointer variable.

#### 5. If I want a variable `p` that can store the address of an int, what type should I declare `p` to be?
For p to be able to store an int, you would use a pointer. It would look like int* p

#### 6. Just like Java, C++ has a `new` command. But C++ also has a `delete` command that Java does not have. Why do we need `delete` in C++, but not in Java? What is `delete` good for?
Java automatically collects garbage after big operations to free up memory, c/c++ on the other hand does not. Delete can be used to free up memory if a big loop stores a lot of data.

#### 7. What is one question about C++ that you would like me to explain in class?
We went over most of the pros and cons of c++/java, but it would be very interesting if you gave us a short big picture overview comparing the two programming languages (like what each would be better for, like maybe c++ is better for gaming and java for databases or something along those lines)
