## task 2
# task 2a
## TITLE  implement class mechanism in java
## source code
```
class myclass {
void displaymessage() {
System.out.println("welcome to java");
}
int add (int a, int b) {
return a+b;
}
public static void main(String[] args) {
myclass obj = new myclass();
obj.displaymessage();
int result = obj.add(10, 20);
System.out.println("sum: " + result);
}
}
```
# OUTPUT
![task 2a 5as](https://github.com/user-attachments/assets/99cb654b-7bd0-4849-a93e-d242654d0a86)

## task 2b
## TITLE implement method overloading in java
## source code
```
class OverloadExample {
int add(int a, int b) {
return (a + b);
}
double add(double a, double b) {
return a + b;
}
int add(int a, int b, int c) {
return a + b + c;
}
public static void main(String[] args) {
OverloadExample obj = new OverloadExample();
int sum1 = obj.add(10, 20);
double sum2 = obj.add(5.5, 6.5);
int sum3 = obj.add(10, 20, 30);
System.out.println("Result of adding two integers: " + sum1);
System.out.println("Result of adding two double values: " + sum2);
System.out.println("Result of adding three integers: " + sum3);
}
}
```
# OUTPUT
![task 2b 5as](https://github.com/user-attachments/assets/25a8b736-e50a-493b-b18a-828b9a5b8dc6)

## task 2c
## TITLE: 2c.) java program implement constructor
## source code
```
class Student {
String name;
int age;
int marks;
Student (String n, int a, int m) {
name = n;
age = a;
marks = m;
}
void display ( ) {
System.out.println ("Name: " + name);
System.out.println ("Age: " + age);
System.out.println ("Marks: " + marks);
}
public static void main(String[] args) {
Student S1 = new Student ("Alice", 20, 85);
S1.display ( );
}
}
```
# OUTPUT
![task 2c 5as](https://github.com/user-attachments/assets/c8a7c156-918f-4645-84eb-8ac4ffbb4df7)
