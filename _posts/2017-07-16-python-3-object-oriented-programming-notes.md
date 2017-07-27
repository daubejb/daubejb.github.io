---
layout: default
title:  Python 3 Object-Oriented Programming Notes
date:  2017-07-16 08:33:45 +0000
categories: notes
tags: howto python object-oriented-programming
---
# Notes from Python 3 Object-Oriented Programming

## Notes

### Chapter One - Object-oriented Design

1. **Object** - a collection of _data_ and associated _behaviors_
2. **Object-oriented** - functionality directed towards modeling objects
3. **Object-oriented analysis (OOA) "What"** - process of looking at a problem, system, or task (that somebody wants to turn into an application) and identifing the objects and interactions between those objects
4. **Object-oriented design (OOD) "How"** - process of converting OOA requirements into an implemntation specification
5. **Object-oriented programming (OOP)** - process of converting OOD design into a working program
6. **Class** - kind of object
7. Classes describe objects, blueprints for creating an object
8. Data typically represents the individual characteristics of a certain object, data is store in attributes
9. **Attribute** - frequently referred to as members of properties
10. Behaviors are actions that can occur on an object
11. **Methods** - The behaviors that can be performed on a specific class of objects / methods are like functions in structured programming, but they magically have access to all the data associated with this object
12. Methods can accept parameters and return values
13. **Parameters** - a list of objects that need to be passed into the method being called
14. **Arguments** - the objects that are passed in from the calling object are usually referred to as arguments 
15. **Interface** - the collection of attributes and methods that other objects can use to interact with that object
16. **Information Hiding** - process of hiding the implementation, or functional details, of an object (aka encapsulation)
17. **Encapsulation** - is, literally, creating a capsule.  And, so think of creating a time capsule
18. The public interface is very important.  It needs to be carefully designed as it is difficult to change it in the future
19. **Abstraction** - dealing with the level of detail that is most appropriate for the given task
20. In OOA, nouns are typically the objects, where, methods typically represent nouns.  Attributes can often be picked up as adjectives
21. **Composition** - the act of collecting several objects together to create a new one.
22. Composition is usually a good choice when one object is part of another object
23. **Aggregation** - aggregation iss almost exactly like composition, the difference is that aggregate objects can exist independently.  Also, if the parent is destroyed, and the child can live on. then the relationship is aggregation
24. Any composite relationship is also an aggregate relationship, but not vice versa
25. **Inheritance** - a class can inherit attributes and methods from another class
26. **Abstract methods** - we demand this method exist in any non-abstract subclass, but we are declining to specify an implementation in this class
27. **Interfaces** - a class that does not implement any methods at all. it simply tells what the class should do, but not advice on how it should do it
28. **Polymorphism** - the ability to treat a class differently depending on which subclass is implemented
29. **duck typing** if it walks like a duck or swims like a duck, its a duck
30. **refactoring** - improve the design by moving code around, removing duplicate code or complex relationships in favor of simpler, more elegant designs

### Chapter Two - Objects in Python

1. **dot notation** - object.attribute = value syntax
2. **docstrings** - the way to write API documentation directly into your code so that you do not have to keep other documentation up to date
3. **modules** - are simply Python files, nothing more
4. **import** - used for importing modules or specific classes or functions from modules
5. **package** - a collection of modules in a folder, the name of the package is the name of the folder
6. To tell python that this folder is a package, simply put an \_\_init\_\_.py file in the folder
7. startup code should always go in a function named 'main'
8. Policy to wrap all scripts in an __if \_\_name\_\_ == "\_\_main\_\_":  main()__ - this way, just in case you write a function you will find useful to be imported by other code someday
9. **Abstraction** - access control is related to abstraction
10. Private attributes or methods, by convention, should be prefixed with an underscore character.  Python programmers will interpret this as "this is an internal variable, think three times before accessing it directly"
11. **name mangling** - prefix with double underscore means thta the method can still be called by outside objects if they really want to do it, but it requires extra work and is a strong indicator that you demand that your attribute remains private
12. **ensurepip** - python does not come with pip; however, ensure pip installs it

### Chapter Three - When Objects Are Alike

1. **Basic Inheritance** - All Python classes are subclasses of the special class named object
2. **mixin** - is generally a superclass that is not meant to exist on its own, but is meant to be inherited by some other class to provide extra functionality.  It is the simplest and most useful form of multiple inheritance
3. **Method Resolution Order (MRO)** - \_\_mro\_\_ can be adapted on the fly to adjust the order in which methods can be called
4. **\*\*kwargs** - basically collects any keyword arguments passed into the method that were not explicitly listed in the parameter list.  These arguments are stored in a dictionary named kwards
  - when we call a different method (for example, _super().\_\_init\_\_)_ with a \*\*kwargs syntax, it unpacks the dictionary and passes the results to the method as normal keyword arguments
5. **Abstract base classes (ABCs)** - define a set of methods and properties that a class must implement in order to be considered a duck-type instance of that class.  The class can extend the abstract base class itself in order to be used as an instance of the class, but it must supply all the appropriate methods

### Chapter Four - Expecting the Unexpected

1. **Exceptiongs** - special error objects that only need to be handled when it makes sense to handle them
2. Exceptions are just objects.  There are many different exception classes
3. All exceptions inherit from **BaseException**
4. In Python **Error** and **Exception** are used interchangeably
5. **raise** - keyword causes an exception to occur
6. When an exception is raised, any lines that were supposed to run after the exception are not executed
7. Exceptions can be handled at any level after they are initially raised

### Chapter Five - When to Use Object-oriented Programming

1. Treat objects as objects - give separate objects in your problem domain a special class in your code
2. Objects are things that have both data a behavior
3. If a script is not meant to be ran directly, remove the main call at the bottom of the original script
4. In python strings aren't mutable (able to be changed).  Once a str is defined, it is forever
5. **\\n** represents the end of one line and the beginning of a new one

### Chapter Six - Python Data Structures

1. Python disables arbitrary attributes on the base class object for memory saving purposes
2. It is possible to restrict arbitrary properties on our own classes using **slots**
3. Again, Classes should be only used when you want to specify _both_ data and behaviors
4. **Tuples** are objects that can store a specific number of other objects in order.  They are immutable
5. If you need to modify a tuple, you are using the wrong data type
6. The primary benefit of tuples' immutability is that we can use them as keys in dictionaries, and in other locaitons where an object requires a hash value
7. The primary purpose of a tuple is to aggregate different pieces of data together into one container
8. Named tuples are tuples with attitude.  It is a great way to group read-only data together
9. Dictionaries are incredibly useful containers that allow us to map objects directly to other objects.  An empty object with attributes are a sort of dictionary.
10. Dictionaries are extremely efficient at looking up a value, given a specific key object that maps to that value
11. **value** - the object that is being stored is called the value
12. **key** - the object that is being used as the index is called the key 
13. **get** method - accepts a key as the first parameter and an option default value if the key doesn't exist
14. **setdefault** method - trys to set the value to the provided if the key does not exist; otherwise provide the already supplied value
15. Dictionaries are unsorted due to the efficient algorithm (known as hashing)
16. Lists cannot be stored in a dictionary

### Chapter Seven - Python Object-oriented Shortcuts

1. **Method Overloading** - having multiple methods with the same name that accept different sets of agrguments.

### Chapter Eight - Strings and Serialization

1. **to read**

### Chapter Nine - The Iterator Pattern

1. **Design patterns** - a design pattern proposes a set of objects interacting in a specific way to solve a general problem
2. **Iterator** - is an object with a next() method and a done() method; the latter returns True if there are no items left in the sequence
3. The abstract base class **Iterator** in the _collections.abc  module_, defines the iterator protocol in Python
  - it must have a \_\_next\_\_ method that the for loop can call to get a new element from the sequence
  - In addition, every iterator must also fulfill the **Iterable** interface
  - any class that provides the \_\_iter\_\_ method is iterable; that method must return an Iterator instance that will cover all the elements in the class
4. **Comprehensions** are simple, but powerful, syntaxes that allow us to transform or filter an iterable objec tin as little as one line of code
5. **List comprehensions** are one of the most powerful tools in Python.  List comprehensions are far faster than for loops when looping over a huge number of items.  Example:
```python
input_strings = ['1', '1', '2', '3', '5', '8']output_integers = [int(num) for num in input_strings]
```








---
