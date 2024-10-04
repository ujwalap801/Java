
# Java Tokens

In Java, **tokens** are the smallest elements of a program that have meaning. They are the building blocks of Java code and are categorized into several types. Below are the main types of tokens in Java:

## 1. Keywords
Keywords are reserved words that have a predefined meaning in Java. They cannot be used as identifiers (names for variables, classes, etc.). Some common keywords include:
- `class`
- `public`
- `static`
- `void`
- `int`
- `if`
- `else`
- `for`
- `while`
- `return`

## 2. Identifiers
Identifiers are names given to entities such as variables, methods, classes, and interfaces. Identifiers must begin with a letter (A-Z or a-z), underscore (_), or dollar sign ($). Subsequent characters may also include digits (0-9). 

### Rules for Identifiers:
- Must not start with a digit.
- Cannot be a keyword.
- Should not contain special characters (except for `_` and `$`).

**Examples**:
- **Valid**: `myVariable`, `sum`, `calculateTotal`, `number_1`
- **Invalid**: `1stVariable`, `class`, `my-variable`

## 3. Literals
Literals are constant values that are directly represented in the code. They can be of various types:
- **Integer Literals**: e.g., `100`, `0xFF` (hexadecimal), `0123` (octal)
- **Floating-point Literals**: e.g., `3.14`, `2.5e10` (scientific notation)
- **Character Literals**: e.g., `'a'`, `'\n'`
- **String Literals**: e.g., `"Hello, World!"`
- **Boolean Literals**: `true`, `false`

## 4. Operators
Operators are special symbols that perform operations on variables and values. They can be categorized into several types:
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Relational Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `&&`, `||`, `!`
- **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`

## 5. Separators (Delimiters)
Separators, also known as delimiters, are symbols that separate different elements in a program. They include:
- **Braces**: `{ }` (used for defining class and method bodies)
- **Parentheses**: `( )` (used for method calls and control flow statements)
- **Brackets**: `[ ]` (used for arrays)
- **Semicolon**: `;` (used to terminate statements)
- **Comma**: `,` (used to separate elements in a list)

## Example Code Demonstrating Tokens
Here’s a simple Java program that illustrates various tokens:

```java
public class TokenExample {
    public static void main(String[] args) {
        // Keywords: public, class, void, int
        int number = 100; // Identifier and Literal
        int sum = number + 50; // Operator and Literal
        
        // Print the sum
        System.out.println("Sum is: " + sum); // String Literal and Operators
    }
}
