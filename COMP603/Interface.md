An interface is a completely "abstract class" that is used  to group related methods with empty bodies
- All methods are default public abstract in interface

*Interface is an abstract base class*!!!

**Keyword is IMPLEMENT**

```java
interface A {
	void show();
	void config();
}

class B implements A {
	public void show(){
		System.out.println(x:"in show");
	}
	public void config(){
		System.out.println(x:"in config");
	}
}

public class Demo {
	public static void main(String[] args){
		A obj;
		obj = new B();
		obj.show();
		obj.config();
	}
}
```
``
Interface A can be an object because you cannot create an object with an interface class but you can if you implement it into another class (Class B)
 

