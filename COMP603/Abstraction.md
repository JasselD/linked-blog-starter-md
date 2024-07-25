Process of hiding a certain details and showing only essential information to the user

**Abstract keyword is a non-access modifier, used for classes and methods**

**Keyword is EXTENDS**

**Abstract Class**
- A restricted class that cannot be used to create objects (to access it, it must be inherited from another class)

**Abstract Method**
- Can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from)
```Java
// Java program to illustrate the 
// concept of Abstraction 
abstract class Shape { 
	String color; 

	// these are abstract methods 
	abstract double area(); 
	public abstract String toString(); 

	// abstract class can have the constructor 
	public Shape(String color) 
	{ 
			System.out.println("Shape constructor called"); 
		this.color = color; 
	} 

	// this is a concrete method 
	public String getColor() { return color; } 
} 
class Circle extends Shape { 
	double radius; 

	public Circle(String color, double radius) 
	{ 

		// calling Shape constructor 
		super(color); 
		System.out.println("Circle constructor called"); 
		this.radius = radius; 
	} 

	@Override double area() 
	{ 
		return Math.PI * Math.pow(radius, 2); 
	} 

	@Override public String toString() 
	{ 
		return "Circle color is " + super.getColor() 
			+ "and area is : " + area(); 
	} 
} 
class Rectangle extends Shape { 

	double length; 
	double width; 

	public Rectangle(String color, double length, 
					double width) 
	{ 
		// calling Shape constructor 
		super(color); 
		System.out.println("Rectangle constructor called"); 
		this.length = length; 
		this.width = width; 
	} 

	@Override double area() { return length * width; } 

	@Override public String toString() 
	{ 
		return "Rectangle color is " + super.getColor() 
			+ "and area is : " + area(); 
	} 
} 
public class Test { 
	public static void main(String[] args) 
	{ 
		Shape s1 = new Circle("Red", 2.2); 
		Shape s2 = new Rectangle("Yellow", 2, 4); 

		System.out.println(s1.toString()); 
		System.out.println(s2.toString()); 
	} 
}

```
The differences between abstraction and  [[Interface]]