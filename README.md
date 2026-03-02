# JavaNotes
This is my Java refresher page when i forget things
Every app has a class name that is the same name as the file.  This is a requirement.
EX:
Java file name: Main.java
Equivalent class name
```
public class Main {}
```

How to run a program:
1. Go to the directory the program lives
2. type in the terminal "javac Main.java"
3. java Main

- Every line of code that runs must be inside the class

The main() method:
It is required by every java program, it is where it starts running.
```
public static void main(String[] args){...}
```
Remember this for methods
1. scope of access
2. who the method belongs to
3. return type

How to output a line of text:
```
System.out.println("Hello World");
```

Reminder: Use "" with strings

There is also System.out.print("") but it doesn't make a new line line println

So if you don't want to make multi line use print.

Comments:
//
/*  */

# Variables
Notice how only String is capitalized it's because it's a class not a primitive.
- String
- int
- float
- char
- boolean

Variable declaration:
type variableName = value;
String name = "Paul";
int age = 20;
float pizzaRating = 3.2;
char initial = 'P';
boolean likesSwimming = true;

How to make constant variables:
Add final before the type.

EX: final String name = "Paul";

String concactination:
Use + 

ints mixed with Variables:
Without parenthesis it will treat numbers as text after the first string.(so order matters)
EX:
```
int x = 5;
int y = 6;

System.out.println("The sum is " + x + y);   // Prints: The sum is 56
System.out.println("The sum is " + (x + y)); // Prints: The sum is 11
```

Multi variable declaration:
Need to be same type.
int x = 5, y = 6, z = 50;

One variable to multi variables:
int x, y, z;
x = y = z = 50;

# Java Naming conventions
- Letters, numbers, underscores, and dollar signs
- Must begin with letter
- Start with lower case letter
- Can start with $ or _
- Case sensitive
- Reserve words aren't allowed

# What are the non primitive data types
- String
- Arrays
- Classes

# What are the primitive data types
|byte|ints from -128 - 127|
|---|---| 
|short|ints from -32,768 - 32,767|
|---|---| 
|int|ints from -2,147,483,648 - 2,147,483,647|
|---|---| 
|long|ints from -9,223,372,036,854,775,808 - 9,223,372,036,854,775,807|
|---|---| 
|float|Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits|
|---|---| 
|double|Stores fractional numbers. Sufficient for storing 15 to 16 decimal digits|
|---|---| 
|boolean|true or false|
|---|---| 
|char|Single ASCII value|
|---|---| 

# Difference between primative and non primative
- Non-Primatives can be null
- Primatives have to contain a value
- Non-Primatives have methods to call

# Var keyword
Introduced in Java 10 (2018) it let's java decide the data type automatically.
- It only works when you assign the value at the same time.
- Nice for complex data types like ArrayList

# Type casting
- Big -> small = narrowing casting
- small -> Big = widening casting

# String 
Reference: https://www.w3schools.com/java/java_ref_string.asp
How to get string length = String.length()
How to find a character:
charAt(index)
indexOf("something")
string1.equals(string2)
trim() removes from beginnging and end

# Scanner notes
The Java Scanner class works by breaking input into chunks called tokens, using a delimiter (whitespace by default), and then providing various methods to read and convert these tokens into specific data types. 

How Scanner Methods Work
The Scanner class provides two main categories of methods: next...() methods for reading specific data types and hasNext...() methods for validating the input. 

1. Token-Based Reading (next...() methods) 
These methods read the next available token and attempt to convert it to the specified data type. They stop reading when they encounter a delimiter. 
- next(): Reads the next single word (string of characters up to the next whitespace delimiter).
- nextInt(): Reads the next token and parses it as an int value. It can handle locale-specific digit groupings and different radices (number bases).
- nextDouble(): Reads the next token and parses it as a double value.
- nextBoolean(): Reads the next token and interprets it as a boolean value (true or false, case-insensitive).

Other data types: The Scanner class also includes methods for other primitive types like 
- nextFloat(),
- nextByte(),
- nextShort(), and
- nextLong()

next().charAt(0): 
While there is no dedicated nextChar() method, this common pattern uses the next() method to get the next token (a single word/character sequence) and then immediately takes the first character of that string using the charAt(0) method. 

2. Line-Based Reading
nextLine(): This method is different from the token-based methods. It reads the entire line of input, including any spaces, up to the end-of-line character (the carriage return/newline character), and then advances the scanner past that line. A common issue arises when mixing next...() and nextLine(), as next...() methods do not consume the newline character, which can cause the subsequent nextLine() call to read an empty string. 

3. Validation Methods
These methods allow you to check the input type before attempting to read it, which helps in robust error handling and prevents exceptions. 

- hasNext(): Returns true if the scanner has another token in its input.
- hasNextInt(): Returns true if the next token can be interpreted as an int.
- hasNextLine(): Returns true if there is another line of input.
- hasNextDouble(): Returns true if the next token can be interpreted as a double, and so on for all data types. 

Key Mechanism
The core mechanism involves:
Reading bytes: The Scanner reads raw bytes from an underlying input source (like System.in, a file, or a string).
Decoding: It converts these bytes into characters using a default or specified character encoding.
Tokenizing: It groups characters into tokens based on a delimiter pattern, which is whitespace by default but can be customized with useDelimiter().
Parsing: The specific next...() methods then parse these tokens into the desired data types (e.g., converting the string "123" into an integer 123). 

# Functional interfaces
- Consumer:
  ```
  import java.util.function.Consumer;
  ```

  Using it:
  ```
  public class ConsumerExample {
    public static void main(String[] args) {

    // Create a Consumer that prints a string to the console

      Consumer<String> printConsumer = s -> System.out.println("Consumed value: " + s);

    // Apply the Consumer's accept method
      printConsumer.accept("Hello, World!"); // Output: Consumed value: Hello, World!
    }
}
  ```


# Maps
Maps are really cool, they a O(1) average search time for keys because it just runs a calculation.

If you want immutable entries, and you want to have then inside before it runs.  Use

.ofEntries();
