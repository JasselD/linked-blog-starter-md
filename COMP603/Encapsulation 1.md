Meaning is to make sure that "sensitive" data is hidden from users.
- Declare class variable/attributes as private
- provide public get and set methods to access and update the value of private variable

**Public**
- Any method(in any class) can access the field

**Private** 
- Only methods in the class can access the field

**Protected** 
- Any method in the same package can access the field, or any derived class

**Default**
- Only methods in the same package can access the field

```Java
// Java Program to demonstrate
// Java Encapsulation

// Person Class
class Person {
	// Encapsulating the name and age
	// only approachable and used using
	// methods defined
	private String name;
	private int age;

	public String getName() { return name; }

	public void setName(String name) { this.name = name; }

	public int getAge() { return age; }

	public void setAge(int age) { this.age = age; }
}

// Driver Class
public class Main {
	// main function
	public static void main(String[] args)
	{
		// person object created
		Person person = new Person();
		person.setName("John");
		person.setAge(30);

		// Using methods to get the values from the
		// variables
		System.out.println("Name: " + person.getName());
		System.out.println("Age: " + person.getAge());
	}
}

```