Static methods/attributes can be accessed without creating object of a class

Static keyword is a **non-access modifier** in Java that is applicable for the following:
- Blocks
- Variables
- Methods
- Classes

**Characteristics**
- Shared memory allocation
	  Static variables and methods are allocated once during program execution, sharing memory among class instances, making them useful for global state maintenance or shared functionality
	  
- Accessible without objects instantiation
	  Static members, which can be accessed without creating a class instance, are useful for providing utility functions and constants that can be used throughout the program
	  
- Associated with class
	  Static members are class-associated, reflecting changes in all instances of the class and accessible using the class name rather than an object reference
	  
- Cannot access non-static members
	  They are not associated with any particular instance of the class
	  
- Can be overloaded, but not overridden
	 Static methods can be overloaded, allowing multiple methods with the same name but different parameters, but cannot be overridden as they are associated with the class

```Java
public class Demo {

//static method
static void m1() {

System.out.println("from m1");

}

public static void main(String[] args) {

//calling m1 without creating any object
m1();

}

}
```

Static Block
```Java
package Main;

  

public class Demo {

//static variable
static int a = 10;

static int b;

//static block
static {

System.out.println("Static block initialized.");

b = a * 4;

}

public static void main(String[] args) {

System.out.println("from main");

System.out.println("Value of a : "+a);

System.out.println("Value of b : "+b);

}

}

//Static block initialized.
//from main
//Value of a : 10
//Value of b : 40
```

Static variables
```Java
package Main;

class Demo {

//static variable
static int a = m1();

//static block
static {

System.out.println("Inside static block");

}

//static method
static int m1() {

System.out.println("from m1");

return 20;

}

public static void main(String[] args) {

System.out.println("Value of a : " +a);

System.out.println("from main");

}

}

//from m1
//Inside static block
//Value of a : 20
//from main
```

Static method
```Java
package Main;

class Demo {

//static method
static int a = 10;

//instance variable
int b = 20;

static void m1() {

a = 20;

System.out.println("from m1");

//cannot make a static reference to the non-static field b
b = 10;

//cannot make static reference to the non static method m2()
m2();

//cannot use super in static
System.out.println(super.a);

}

//instance method
void m2() {

System.out.println("from m2");

}

public static void main(String[] args) {

//main method

}

}
```

Static vs non-static
![[Pasted image 20240726135527.png]]
