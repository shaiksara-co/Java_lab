## additional exps
# addexp2
## TITLE fibonacci series
```
import java.util.Scanner;

class Fibonacci {
    int sum;
    int n;
    int firstNumber;
    int secondNumber;
    int thirdNumber;

    Fibonacci(int number) {
        n = number;
        firstNumber = 0;
        secondNumber = 1;
        thirdNumber = 0;
        sum = 0;
    }

    void generate() {
        if (n > 0) {
            System.out.print("Fibonacci series: ");
        }

        while (n > 0) {
            if (n == 1) {
                System.out.println(firstNumber + ".");
                sum = sum + firstNumber;
            } else {
                System.out.print(firstNumber + ", ");
                sum = sum + firstNumber;
            }

            thirdNumber = firstNumber + secondNumber;
            firstNumber = secondNumber;
            secondNumber = thirdNumber;
            n--;
        }

        System.out.println("Sum of Fibonacci series = " + sum);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the value of n: ");
        int number = sc.nextInt();

        Fibonacci f = new Fibonacci(number);
        f.generate();
    }
}
```
# OUTPUT

![addexp1](https://github.com/user-attachments/assets/12caef9b-c638-4964-9a44-63c5170128ee)

# addexp1
## TITLE insert substr to mainstr
```
import java.util.Scanner;

class SubstringInsert {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String mainString;
        String subString;
        int position;

        System.out.print("Enter the main string: ");
        mainString = sc.nextLine();

        System.out.print("Enter the substring: ");
        subString = sc.nextLine();

        System.out.print("Enter the position to insert: ");
        position = sc.nextInt();

        int length = mainString.length();
        String resultString;

        if (position >= 0 && position <= length) {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            resultString = firstPart + subString + secondPart;

            System.out.println("Resultant String = " + resultString);
        } else {
            System.out.println("Substring cannot be inserted.");
            System.out.println("Condition: 0 <= position <= " + length);
        }

        sc.close();
    }
}
```
# OUTPUT
![addexp1](https://github.com/user-attachments/assets/c5d2c085-46c3-4cc6-a1f1-3779c4a62756)

