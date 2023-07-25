![[Pasted image 20230725144408.jpg]]


There are three types of variables based on the scope of variables in C++

- **Local Variables**
- **Instance Variables**
- **Static Variables**

1. **Local Variables**: A variable defined within a block or method or constructor is called a local variable. 
    - These variables are created when entered into the block or the function is called and destroyed after exiting from the block or when the call returns from the function.
    - The scope of these variables exists only within the block in which the variable is declared. i.e. we can access this variable only within that block.
    - Initialization of Local Variable is Mandatory.
2. **Instance Variables**: Instance variables are non-static variables and are declared in a class outside any method, constructor, or block. 
    - As instance variables are declared in a class, these variables are created when an object of the class is created and destroyed when the object is destroyed.
    - Unlike local variables, we may use access specifiers for instance variables. If we do not specify any access specifier then the default access specifier will be used.
    - Initialization of Instance Variable is not Mandatory.
    - Instance Variable can be accessed only by creating objects.
3. **Static Variables**: Static variables are also known as Class variables. 
    - These variables are declared similarly as instance variables, the difference is that static variables are declared using the [static keyword](https://www.geeksforgeeks.org/static-keyword-cpp/) within a class outside any method constructor or block.
    - Unlike instance variables, we can only have one copy of a static variable per class irrespective of how many objects we create.
    - Static variables are created at the start of program execution and destroyed automatically when execution ends.
    - Initialization of Static Variable is not Mandatory. Its default value is 0
    - If we access the static variable like the Instance variable (through an object), the compiler will show the warning message and it won’t halt the program. The compiler will replace the object name with the class name automatically.
    - If we access the static variable without the class name, the Compiler will automatically append the class name.

## Instance Variable Vs Static Variable

- Each object will have its **own copy** of the instance variable whereas We can only have **one copy** of a static variable per class irrespective of how many objects we create.
- Changes made in an instance variable using one object will **not be reflected** in other objects as each object has its own copy of the instance variable. In the case of static, changes **will be reflected** in other objects as static variables are common to all objects of a class.
- We can access instance variables **through object references** and Static Variables can be accessed **directly using the class name.**
- The syntax for static and instance variables:

```
class Example
{
    static int a; // static variable
    int b;        // instance variable
}
```

