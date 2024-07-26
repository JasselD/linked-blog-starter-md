Array
Used to store multiple values in a single variable, instead of declaring separate variables for each value

**Variable type is defined by using [square brackets]**

Example:
```Java
String[] cars;

String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

You can access the array with println
```Java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.println(cars[0]);
//output would be Volvo
```

Array size never changes once created

Example:
```Java
public class ArrayVsArrayList{
	public static void main(String[] agrs){
		String[] friendsArray = new String[3];
		//The size of the array is set to 3
		String[] friendsArray2 = {"John", "Chris", "James", "Hans"};
		//This method is to set the values now rather than later
	}
}
```