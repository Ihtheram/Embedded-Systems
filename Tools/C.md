# C Programming Language

#### **[⇐ Embedded Engineering Tools](../Embedded-Engineering-Tools.md)**
---

### Variable Declaration Format: 

```C
type-qualifier(s) type-modifier data-type variable-name = initial-value;
```

Examples:

```C
const unsigned char foo = 12;
```

```C
long int foo;
foo = 400;
```

---
### Type Qualifiers
* `const` Constant
* Volatile
* Restrict

### Modifier
* `short`
* `long`
* `unsigned`
* `signed`

### Data Types

* Basic Data Types

    * `int`: Integer type, typically used for whole numbers.
    * `char`: Character type, used to store a single character.
    * `float`: Floating-point type, used for decimal numbers.
    * `double`: Double-precision floating-point type, for more precise decimal numbers.

* Derived Data Types

    * Arrays: A collection of elements of the same type.
    * Structures: A user-defined data type that groups different data types.
    * Unions: Similar to structures, but can store different data types in the same memory location.
    * Pointers: Variables that store memory addresses of other variables.

* Enumeration Type

    * `enum`: A user-defined type that consists of a set of named integer constants.

* Void Type

    * `void`: Represents the absence of value or type, often used in functions that do not return a value.


### Variable sizes
* `char` 1 byte
    - `signed` -128 to 127
    - `unsigned` 0 to 255
* `int` 2 or 4 bytes
    - 16 bit microcontroller (2 bytes)
        - -32,768 to 32,768
        - `unsigned` 0 to 65,535
    - 32 bit microcontroller (4 bytes)
        - -2,147,483,648 to 2,147,483,647
        - `unsigned` 0 to 4,294,967,295
* `short` 2 bytes
    - -32,768 to 32,768
    - `unsigned short` 0 to 65,535
* `long` 4 bytes
    - -2,147,483,648 to 2,147,483,647
    - `unsigned long` 0 to 4,294,967,295

⁰, ¹, ², ³, ⁴, ⁵, ⁶, ⁷
### Number Conversion
* 0b10010101 (Unsigned)

    = 1 * 2⁷ + 0 * 2⁶ + 0 * 2⁵ + 1 * 2⁴ + 0 * 2³ + 1 * 2² + 0 * 2¹ + 1 * 2⁰

    = (128 + 16 + 4 + 1)₁₀

    = (149)₁₀

* 0b10010101 Signed 2's

    = -(1 * 2⁷) + 0 * 2⁶ + 0 * 2⁵ + 1 * 2⁴ + 0 * 2³ + 1 * 2² + 0 * 2¹ + 1 * 2⁰

    = (-128 + 16 + 4 + 1)₁₀

    = (-107)₁₀

### Operators
* Logical ||, &&, !
* Bitwise <<, >>, |, &, ^ (Bitwise XOR), ~ (One's Complement)
    
    - **>>** (Right-Shift)
    ```C
    int varA = 0b10010110;
    
    varA >> 4; // Right-Shift 4 bits
    // = 0b10010110
    // = 0b00001001
    
    // Zeroes shifted in from the left
    // lower bits (after 8th) truncated
    
    ```
    
    - **&** (Bitwise-AND)
    ```C
    foo = varA & varB;

    varA = 0xF5; // -----> 1 1 1 1 0 1 0 1
    varB = 0x5B; // -----> 0 1 0 1 1 0 1 1
    //------------------------------------
    foo = 0x51;  // -----> 0 1 0 1 0 0 0 1
    ```

* Arithmetic +, -, /, *, ++, --, %
* Relational <, <=, >, >=, ==, !=

[Bitwise and Arithmetic operators can be combined with assignment operator (=) for simple expressions]


## Control Flow
* if-else
* while
* loops
    - for
    - do-while / while

## Functions

* Function Declaration Format
```C
function-type function-name(param1-type param1, param2-type param2, ...);
```
* Function Definition Format
```C
function-type function-name(param1-type param1, param2-type param2, ...) {
    // code for the function
}
```

### Headers
* Header (.h) files
    - Contain **public** function declarations
* Implementation (.c) files
    - Contain **private** function declarations
    - Contain all function **definitions** 

### Parameter Passing
* Pass by value
    - Passing a value through function parameter
    - Function gets a copy of the variable that is passed through the parameter.
* Pass by reference
    - Referencing the variable's original address by passing a pointer through the parameter
    - Function gets the ability to modify the original variable.

### Scopes
* Local Scope
    - Variables that are declared inside the function
    - Only accessible from within the function
* Global Scope
    - Variables that are declared outside any function
    - Accessible from anywhere
---

## Pointers

* Pointer declaration operator *
    - data-type * pointer-variable;
    - int * ptr;
* Address-of operator &
    - pointer-variable = &variable;
    - ptr = &foo; (suppose int foo = 0x34;)
* Dereference Operator *
    - *pointer-variable = value;
    - *ptr = 0x52; (modifies foo's original value)


## C Standardization and Team Coding Standards

Standards provide specific syntax and features what each version of the language supports.

**Standards Organizations**

* International Electrical and Electronics Engineers (IEEE)
* International Organization for Standardization (ISO)
* American National Standards Institute (ANSI)

are three groups that are involved with the process of standardizing various technical ideas including software.

**C-Programming Standards**
* K&R C-Programming
    - Informal Standard
    - Late 1970's
* C89 (ANSI-C) / C90 (ISO-C)
* C99
* C11

## **Coding Standards / Guidelines**

Rules developers adhere to in order to make changes to code. A coding standards is simply a list of software guidelines a project will need to be written to. These standards can be a mixture of requirements which may include

* Special format and documentation of the code  
* Programming the flow of routines in a certain way
* Naming functions, files, and variables following a certain scheme
* Limits on the types of features a developer can use on a platform.

Benefits of Coding Standards:
* Makes code readable
* Improves runtime efficiency
* Ensures consistency between various coders
* Preventing bugs
* Reducing Bad Practices
* Helps protect copyright claims
* Ensuring security, portability, reliability and safety of software

### C-Programming Coding Guidelines

* **MISRA C** Coding Guideline
    - by Motor Industry Software Reliability Association
* Jack Ganssle's **Firmware Development Standard**


### Sample Code Example with Coding Guidelines
In this code example we will see a variety of example coding guidelines as discussed in the associated reading on Jack Ganssle's A Firmware Development Standard. 

* Starting at the top of the file with a block of comments that discuss file name or module name, some copyright information, authorship and a description of the module.

* An informative header section can save a developer a lot of time tracking down information in the code.

The copyright listed in this section is also very important for a software engineer to read and understand, especially when looking into adding third party software into your project. Including software in a project without checking copyright could cause major issues. Copyright infringement may lead to the loss of ownership of the code and other legal issues.

```C
/**************************************************
* Version Module - Project SAMPLE
*
* Copyright 1997 Company
* All Rights Reserved
*
* The information contained herein is confidential
* property of Company. The use, copying, transfer or
* disclosure of such information is prohibited except
* by express written agreement with Company.
*
* 12/18/97 - Version 1.3 - ROM ID 78-130
* Modified module AD_TO_D to fix scaling
* algorithm; instead of y=mx, it now
* computes y=mx+b.
* 10/29/97 - Version 1.2 - ROM ID 78-120
* Changed modules DISPLAY_LED and READ_DIP
* to incorporate marketing’s request for a
* diagnostics mode.
* 09/03/97 - Version 1.1 - ROM ID 78-110
* Changed module ISR to properly handle
* non-reentrant math problem.
* 07/12/97 - Version 1.0 - ROM ID 78-100
* Initial release
**************************************************/
# undef VERSION
# define VERSION “Version 1.30”
```