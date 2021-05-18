This repository is ARCHIVED. More up to date and organized content can be found here:

https://www.nexulacademy.com/courseware/csharp-introduction

C# Cheatsheet
===============

C# is pronounced as 'see sharp'.

C# can be used to create almost anything but is particularly strong at building Windows desktop applications and games, 
web application middle tier APIs and has become increasingly popular for mobile development with Xamarin. C# was created 
by Microsoft and is now an open source platform that runs on Windows, Linux and Mac.

Variables
---------

Variables are containers for data in your code. They help you refer to a value by name, so that you can then use that value again
in an expression modifying that value or to modify other values. If you can't give something a name, how else could you build more
complex ideas?

Variables are defined in C# as:

    string message;

This defines a variable called 'message'. The keyword 'string' means that the variable can only hold a string, 
and not a number or any other type.

Assignment of a value:

    string message = "Hello";
    message = "Hello World";
    
The 'var' keyword can replace any datatype, as long as the compiler can infer what the underlying datatype is. 

    var message = "Hello";

Data types
----------

There are many types of data in C#. The first category is value types.

    bool isEmployee; // a true/false value;
    isEmployee = true;
    isEmployee = false;
    
    int count; // an alias for Int32
    count = 5;
    Int32 count2 = 7;
    Int64 count3 = 27364; // 64-bit number, holds larger values
    Int16 count4 = 45; // a 16-bit number, for small numbers
    
    double numX = 45.2;

Any many more here:
https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/types-and-variables
    
You can define custom datatypes as a 'class'.  Let's get back to that later.

Math
----

Mathmatical operators let you combine variables containing multiple values into a new variable or to replace an existing variable value.


    var x = 5;
    var y = x + 3;
    Console.WriteLine("y is " + y);

    var b = x - 2;
    var c = x * 2;
    var d = 2 / 2;
    var m = 10 % 2;
    Console.WriteLine(m + " is the value of m");
          

String concatenation
--------------------

You can combine strings in a few ways.

* adding them together with the plus operator
* string.Format() method
* string interpolation

        static void DoSomething()
        {
            var x = 5;
            var y = x + 3;
            Console.WriteLine("y is " + y);

            var s0 = string.Format("The value of y is {0}", y);
            Console.WriteLine(s0);

            var s1 = $"The value {x} is in variable x";
            Console.WriteLine(s1);
        }


Methods (functions)
-------------------

A method is equivalent to functions or procedures in other languages. A method is always defined in a class. 

    class Program
    {
        static void Main()
        {
            var x = 5;
            var y = x + 3;
            Console.Write("y is " + y);
        }
    }


The first keyword 'public' is the scope of the method, or in other words, what code can see and call it.  use 'public' until you find a need for the others, "private", "protected" and "internal".

* private:  only the class defining the method can see/use it.
* public: any code that can see the class can use it.
* protected: like private, but also visibe to 'derived' classes.
* internal: like private, but also visible to any other code in the same project.

The second part is the return datatype of the method call.  Use 'void' if the method does not return a value.

Inside method parenthesis, you can define required parameters (arguments) to be used. You cannot use 'var' as the type of a method
parameter.

    public int Add(int x, int y)
    {
        return x + y;
    }

Classes
-------

      public class Employee
      {
          public string FirstName { get; set; }
          public string LastName { get; set; }
      }

Usually, classes are defined in a separate file each, named the same as the class name and with a ".cs" file extension.
File names are not required to match, and multiple CAN be in the same file.

You can define a variable of a class type the same as any value type. However, creating a new value requires the 'new' keyword.

    Employee emp1;
    emp1 = new Employee();
    Employee emp2 = new Employee();

You can interact with a class' properties with the "dot" syntax.

    var emp3 = new Employee();
    emp3.FirstName = "Mary";
    emp3.LastName = "Smith";
    
The parenthesis after 'new Employee()' are a method call to the 'constructor' method of the class. Every class has an implied
constructor that does nothing, unless you create a constructor yourself. You can add additional parameters that take values as
any other method would do.

      public class Employee
      {
          public string FirstName { get; set; }
          public string LastName { get; set; }
          
          public Employee()
          {
          }
          
          public Employee(string firstName, string lastName)
          {
              this.FirstName = firstName;
              this.LastName = lastName;
          }
      }


Further resources
-----------------

Follow along creating a tic-tac-toe game in a C# console app with this workshop:
https://github.com/NexulAcademy/intro-csharp-tictactoe
