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
