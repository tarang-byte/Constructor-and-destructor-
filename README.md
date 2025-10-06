# Constructor-and-destructor-
# Constructors-and-Destructors-in-cpp

# Aim:
To study and implement Constructors and Destructors.

# Tools Used: 
VS Code.

# Theory:

# Constructors in Cpp:
  
A constructor in C++ is a special member function of a class that is automatically called when an object of the class is created. Its primary purpose is to initialize the data members of the class.

# Default Constructor:

No parameters, used to set default values or take input.
class Student {

int prn;
public:

Student() {  // default constructor
}

# Parameterized Constructor:
 Takes parameters to set values at the time of object creation.

class Student { int prn; public: Student(int a) { // parameterized constructor prn = p; } };

# Copy Constructor:
 Creates a new object by copying the data of an existing object.

class Student { int prn; public: Student(int p) { prn = p; } Student(const Student &s) { // copy constructor prn = s.prn; } };

# Destructors in Cpp:

A destructor is a special member function in C++ that is automatically called when an object goes out of scope or is explicitly deleted. Its main purpose is to release resources that the object may have acquired during its lifetime.

class Student { public: ~Student() { // destructor cout << "Destructor called, object destroyed" << endl; } };

# Program 1:Default Constructor (In-class)
Explanation:
The class Marks has its default constructor defined inside the class. When an object is created, it prompts the user for details and stores them. Demonstrates how in-class constructors handle initialization.

# Algorithm:

1.Start.

2.Define a class Marks with five integer data members: SS, EDC, DCLD, NT, MTT.

3.Inside the class, define a default constructor to take input for all members.

4.In main(), create an object of Marks.

5.Stop.

# Program 2: Default Constructor (Out-class)
Explanation:
The default constructor is declared inside the class but defined outsid using the scope resolution operator ::. When the object is created, it accepts employee details. A separate display() function shows stored information, illustrating separation of declaration and definition.

# Algorithm:
1.Start.

2.Define a class Date:

3.int day

4.int month

5.int year

6.Declare a default constructor Date() in the class.

7.Declare a member function display() to show the date.

8.Define the constructor Date():

9.Prompt the user to enter day, and read the value into day.

10.Prompt the user to enter month, and read the value into month.

11.Prompt the user to enter year, and read the value into year.

12.In the main() function: Create an object d of class Date.

13.End.

# Program 3: Parameterized Constructor
Explanation:
This program defines a class Num with two integers as data members. It uses a parameterized constructor to initialize the values of num1 and num2 at the time of object creation. The display() function is used to print these values. In main(), when object n1 is created with values (45, 21), the constructor sets them, and display() outputs the result.

# Algorithm:
1.Start

2.Define a class Num with two integer data members: num1 and num2.

3.Define a parameterized constructor Num(int a, int b) that: --Assigns a to num1. --Assigns b to num2.

4.Define a member function display() that prints the values of num1 and num2.

5.In the main() function: --Create an object n1 of class Num by passing values (23, 78) to the constructor. --Call n1.display() to output the stored values.

6.End

# Program 4: Copy Constructor
Explanation:
This program demonstrates the use of a copy constructor in C++. The class Num has two integers that are initialized either through a parameterized constructor or by copying another object. When object n2 is created from n1, the copy constructor is called, and it duplicates the values of n1 into n2. The display() function prints the values of both objects.

# Algorithm:
1.Start

2.Define a class Num with two integer data members: num1 and num2.

3.Define a parameterized constructor Num(int a, int b) that assigns a to num1 and b to num2.

4.Define a copy constructor Num(const Num &n) that copies the values of num1 and num2 from another object n and prints "Copy constructor is called!".

5.Define a member function display() that outputs the values of num1 and num2.

6.In the main() function: --Create object n1 with values (23, 78) using the parameterized constructor. --Call n1.display() to print its values. --Create another object n2 as a copy of n1. The copy constructor is invoked automatically. --Call n2.display() to print the copied values.

7.End

# Program 5: Copy Constructor
Explanation:
This program defines a class Book with data members for book name, author, and price. It uses a parameterized constructor to initialize these details when an object is created. A copy constructor is also defined, which duplicates the values of one object into another and prints a message. In main(), book details are entered, stored in object b1, displayed, and then copied into b2 using the copy constructor.

# Algorithm:
1.Start

2.Define a class Book with three data members: name (string), author (string), and price (float).

3.Define a parameterized constructor Book(string b, string a, float p) that assigns the values of book name, author, and price.

4.Define a copy constructor Book(const Book &b) that copies the data members from another object and prints "Copy constructor is called!".

5.Define a member function display() that outputs the book details.

6.In the main() function: --Take input from the user for book name, author, and price. --Create object b1 using the parameterized constructor and display its details. -- Create another object b2 as a copy of b1, which automatically calls the copy constructor. --Display the details of b2.

7.End

# Program 6: Destructor
Explanation:
This program demonstrates the use of constructors and destructors with a static counter. Each time a Book object is created, the constructor increments count and displays the number of objects. When an object goes out of scope, the destructor is called, decrementing count and showing how many objects remain. It illustrates object creation and destruction order in C++.

# Algorithm:
1.Start

2.Initialize a global variable count = 0.

3.Create a class Book with:

4.Constructor → increments count and prints message.

5.Destructor → decrements count and prints message.

6.In main(), create multiple objects, including one inside a local block.

7.Observe creation and destruction messages in sequence.

8.End

# Program 7: Destructor
Explanation:
This program shows the working of a destructor in C++. The class Date has only a destructor, which prints "Destructor Called" whenever an object is destroyed. In main(), four objects (d1, d2, d3, d4) are created, and additional temporary objects are created inside the loop. As each object goes out of scope, its destructor is automatically invoked. Here, constructor isn't specifically written but, by default constructor is present in the code.

# Algorithm:
1.Start

2.Define a class Date with a destructor that prints "Destructor Called" whenever an object is destroyed.

3.In the main() function: --Create four objects d1, d2, d3, d4. --Enter a for loop that runs 4 times (i = 0 to 3). --In each iteration, create a temporary object d1 inside the loop. --At the end of each iteration, the loop’s local object d1 goes out of scope, and its destructor is called.

4.After the loop ends, when main() completes, the destructors of d1, d2, d3, d4 (created outside the loop) are invoked automatically in reverse order of creation.

5.End

# Conclusion
We have learned how to use default, parameterized, and copy constructors to initialize objects in various ways. Additionally, I observed the role of destructors in cleaning up resources and tracking the object lifecycle. These concepts are fundamental for effective resource management in object-oriented programming.
