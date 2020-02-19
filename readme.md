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
    
You can define custom datatypes as a 'class'.

Classes
-------

      public class Employee
      {
          public string FirstName { get; set; }
          public string LastName { get; set; }
      }
      
