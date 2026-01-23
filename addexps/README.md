![addexp3](https://github.com/user-attachments/assets/b0a851a9-4f59-48d4-9757-338fc144cd6d)## additional exps
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

# addexp3
## TITLE palindrome
```
import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the string: ");
        String str = sc.nextLine();

        int start = 0;
        int end = str.length() - 1;
        boolean flag = true;

        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                System.out.println("String is not a palindrome");
                flag = false;
                break;
            }
            start++;
            end--;
        }

        if (flag) {
            System.out.println("String is a palindrome");
        }

        sc.close();
    }
}
```
# output
![addexp3](https://github.com/user-attachments/assets/616013f4-9809-4b31-a4f8-aba4e9bd7f29)

# addexp4
## TITLE perfect no or not
```
import java.util.Scanner;

class Perfect {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the positive number: ");
        int num = sc.nextInt();

        int sum = 0;

        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        if (sum == num && num != 0) {
            System.out.println(num + " is a Perfect Number");
        } else {
            System.out.println(num + " is not a Perfect Number");
        }

        sc.close();
    }
}
```
# OUTPUT
![addexp4](https://github.com/user-attachments/assets/52c34474-7f27-4128-83ef-9b72f901b95b)


