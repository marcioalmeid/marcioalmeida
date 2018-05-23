Studies about Lambda Java 8

Functional interface
is an interface that contains only one abstract method.

The Arrow operator
In Java lambda a new arrow operator -> was introduced divides the lambda expression in two parts
(n) -> n*n
The right side specify the action of the lambda expression, in the other words n becames n*n


Block Lambdas
When the arrow operator has more than one statement 
MyString reverseStr = (str) -> {
		String result = "";
		 for(int i = str.length()-1; i >= 0; i--)
			result += str.charAt(i);		
		return result;
	};

Generic Functional Interfaces

A lambda expression cannot be generic but the functional interfaces with his lambda expression can.
Example from https://medium.freecodecamp.org/learn-these-4-things-and-working-with-lambda-expressions-b0ab36e0fffc
interface MyGeneric<T> {
	T compute(T t);
}
public static void main(String args[]){
	// String version of MyGenericInteface
	MyGeneric<String> reverse = (str) -> {
		String result = "";
		for(int i = str.length()-1; i >= 0; i--)
			result += str.charAt(i);
		return result;
	};

	// Integer version of MyGeneric
	MyGeneric<Integer> factorial = (Integer n) -> {
		int result = 1;
		for(int i=1; i <= n; i++)
			result = i * result;		
		return result;
	};
  
  // Output: omeD adbmaL
	System.out.println(reverse.compute("Lambda Demo")); 

	// Output: 120
	System.out.println(factorial.compute(5))
  
  
  
