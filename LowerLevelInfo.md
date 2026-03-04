Java runs in the JVM, esentially it's a virtual environment, so you are sitting on top of the actual hardware and don't have direct access to the hardware and system.

As a reminder, you can run terminal commands with java.  Using the ProcessBuilder, or the Runtime.getRuntime().exec() classes.

# JNI
The java native interface lets you use different programming languages like c or c++

What is an interface?
- Has methods and variables like classes, but the methods are abstract (only the method signature, nothing inside aka no body)
- They specify what the class must do, but not how.  

```
interface interface_name {
  //declare constant fields
  //declare methods that abstract
  //by default
}
```

Example
```
// interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void run(); // interface method (does not have a body)
}
```

To access the interface metods the interface has to be implemented by another class with **implements**, and the body of the interface method is provided by the implementation class.
Like this:
```
interface Animal {
  public void animalSound();
  public void sleep();
}

class Pig implements Animal {
  public void animalSound(){
    System.out.println("Oink Oink!");
  }

  public void sleep(){
    System.out.println("zzzzz");
  }
  
}
```

What are native methods?  They are methods written in java but implemented in another language.

Here is how it's run:
- A header file of the native language is created
- Implement the native method in that language header file
- Load the library in the java code and no error will show in the program

Here is the main file

```
//Java native interface
import java.io.*;

//Driver class
class Middleman {
  public native void printHello();

  //Load the native library
  static{
    System.loadLibrary("hello");
  }

  //Main method
  public static void main(String[] args){
    System.out.println("In this program we will learn about java native");
    //Create an instance of Middleman and call the native method
    Middleman middleman = new Middleman();
    middleman.printHello();
  }
}
```
- System.loadLibrary() method in Java is used to load a native library dynamically, specified by a library name (e.g., "mylib") rather than a complete path. The Java Virtual Machine (JVM) then automatically determines the platform-specific name (e.g., libmylib.so on Linux, mylib.dll on Windows) and location to load the library from the system's library path.
- 
