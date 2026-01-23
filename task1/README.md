##task 1
#task 1a
## Default values of primitive datatypes
experiment1
## TITLE: 1a.) Display the Primitive datatypes 
```
class Datatypes{
static byte b;
static short s;
static int i;
static double d;
static float f;
static char c;
static boolean bool;
public static void main(String[]args) {
System.out.println("default primitive Datatypes:");
System.out.println("byte:"+b);
System.out.println("short:"+s);
System.out.println("int:"+i);
System.out.println("double:"+d);
System.out.println("float:"+f);
System.out.println("char:"+c);
System.out.println("boolean:"+bool);
}
}
```
# OUTPUT
![task1a 5as](https://github.com/user-attachments/assets/30c2cdb7-1ca9-490d-9ac3-cd594b141ba3)

#task 1b
## Roots of a quadratic eqn
```
import java.util.Scanner;
class QuadraticRoots {
public static void main(String[] args) {
double a,b,c,D;
Scanner sc = new Scanner(System.in);
System.out.print("Enter value of a: ");
a=sc.nextDouble();
System.out.print("Enter value of b: ");
b=sc.nextDouble();
System.out.print("Enter value of c: ");
c=sc.nextDouble();
D=b*b-4*a*c;
System.out.println("Discriminant(D)="+D);
if (D>0) {
double x1 = (-b+Math.sqrt(D))/(2*a);
double x2 = (-b-Math.sqrt(D))/(2*a);
System.out.println("Roots are real and distinct.");
System.out.println("Rootl="+x1);
System.out.println("Root2="+x2);
} else if (D==0) {
double x=-b/(2*a);
System.out.println("Roots are real and equal.");
System.out.println("Root="+x);
} else {
double real=-b/(2*a);
double imaginary = Math.sqrt(-D)/(2*a);
System.out.println("Roots are imaginary (complex).");
System.out.println("Rootl="+real+"+1"+imaginary);
System.out.println("Root2="+real+"-1"+imaginary);
}
sc.close();
}
}

```
# OUTPUT
![task1b 5as](https://github.com/user-attachments/assets/e2ab83af-b90d-4542-bb8d-63b877b9f612)

