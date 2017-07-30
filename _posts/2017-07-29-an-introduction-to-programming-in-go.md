# An Introduction to Programming in Go
by Caleb Doxsey
[http://www.golang-book.com/books/intro](http://www.golang-book.com/books/intro)

## My Notes:

### Chapter 1 - Getting Started

1. **No notes**
---

### Chapter 2 - Your First Program

1. Two types of Go programs:  executables and libraries
  - executable applications are the kinds of programs that we can run directly from terminal
  - libraries are collections of code that we package together so that we can use them in other programs
2. Go mostly does not care about whitespace
3. **fmt** - the Go package that implements formatting for input and output
4. **Double quotes** - is a string literal, which is a type of "expression"
5. // represents the beginning of a comment, /* asdfasfasdfasdf */ can be used for a multi line comment
6. **main** - is the function that is called when we execute the program
7. **Println** - is a function inside of _fmt_ that means 'print line'
8. **godoc** package function - brings back the information about the given function
9. **go run** filename.go - runs the filename.go in terminal

---

### Chapter 3 - Types

1. Go is a statically typed programming language.  This means that variables always have a specific type and that type cannot change
2. **Integers** - Go has the following integer types:
  - uint8 (byte)
  - uint16
  - uint32 (rune)
  - uint64
  - int8
  - int16
  - int32
  - int64
    - the numbers tell us how many bits each of the types use
3. **uint** - means "unsigned integer"
  - unsigned integers contain only positive numbers (or zero)
4. **int** - means "signs integer"
5. Three machine dependent integer types:
  - uint, int, and uintptr - there size depends on the type of architecture you are using
6. **floating point** - are numbers that contain a decimal component (real numbers)
  - floating point numbers are inexact
  - they have a certain size (32 bit or 64 bit)
  - using a larger sized floating point number increases it's precision (how many digits in can represent)
7. Go has two floating point types:
  - float32 (aka, single precision)
  - float64 (aka, double precision)
8. Go has two additional types for representing complex numbers (numbers with imaginary parts):
  - complex64
  - complex128
9. **string** - is a sequence of characters with a definite length use to represent text.
10. Go strings are made up of individual bytes, usually one for each character
11. String literals can be made using double quotes "Hello World" or back ticks \`Hello World\`
12. Double quoted strings cannot contain newlines and the allow for escape sequences
  - \n gets replaced with a newline
  - \t gets replaced with a tab character
13. **fmt.Println("Hello World"[1])** -  yields 101 - because the line says, "give me the index 1 or position 2 element from the string, and the element is represented by a byte (integer)
14. **Boolean** - named after George Boole, is a special 1 bit integer type used to represent true and false (or on and off)
15. Three logical operators are used with boolean values:
  - && - and
  - || - or
  - ! - not
  ---

### Chapter 4 - Variables

1. **variables** - format is _var_ space _name_ space _type_
  - example:  var x string
2. **==** - is just like python - meaning like
3. **short variables** - x := "Hello World" - the go compiler infers the type based on the literal value you assign the variable
4. **Name a variable**
  - must start with a letter
  - may contain numbers or the \_(underscore) symbol
5. Go is lexically scoped using blocks - meaning that variables exist within the nearest curly braces {}
6. **Constants** - variables whose values cannot be changed later - create using _const_ instead of _var_

---

### Chapter 5 - Control Structures

---

### Chapter 6 - Arrays, Slices and Maps

---

### Chapter 7 - Functions

---

### Chapter 8 - Pointers

---

### Chapter 9 - Structs and Interfaces

---

### Chapter 10 - Concurrency

---

### Chapter 11 - Packages

---

### Chapter 12 - Testing

---

### Chapter 13 - The Core Packages

---

### Chapter 14 - Next Steps
