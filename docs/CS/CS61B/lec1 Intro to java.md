# Lecture 1: Introduction to Java

## Comparing Java with Python

### Hello World Example
=== "Python"
	```python
	print("hello world")
	```

=== "Java"
	```java
	public class HelloWorld {
		public static void main(String[] args) {
			System.out.println("hello world");
		}
	}
	```
1. All code in Java must be part of a class.
2. We delimit the beginning and end of segments of code with `{}`.
3. All statements in Java must end with a semicolon.
4. For code to run, we need `public static void main(String[] args)`.

**Running a Java Program**
```sh
$ javac HelloWorld.java
$ java HelloWorld
Hello World!
```

### While Loop Example
=== "Python"
	```python
	x = 0
	while x < 10:
		print(x)
		x = x + 1
	```

=== "Java"
	```java
	public class HelloNumbers {
		public static void main(String[] args) {
			int x = 0;
			while (x < 10) {
				System.out.println(x);
				x = x + 1;
			}
		}
	}
	```
1. Before Java variables can be used, they must be declared.
2. Java variables must have a specific type.

### Function Example
=== "Python"
	```python
	def larger(x, y):
		if x > y:
			return x
		return y

	print(larger(5, -10))
	```

=== "Java"
	```java
	public static int larger(int x, int y) {
		if (x > y) {
			return x;
		}
		return y;
	}
	```
1. Java functions must specify the return type.
2. Java functions must declare the type of each parameter.
