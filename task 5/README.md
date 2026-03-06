
## task 5
# task 5a
## AIM: To write a JAVA program to implement Interface.
 ```
java

// Sortable.java
public interface Sortable {
    void sort(int[] arr);
}

// BubbleSort.java
public class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}

// SelectionSort.java
public class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            int min = i;
            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[min]) {
                    min = j;
                }
            }
            int temp = arr[min];
            arr[min] = arr[i];
            arr[i] = temp;
        }
    }
}

// TestSort.java
import java.util.Scanner;

public class TestSort {

    static void printArray(int[] arr) {
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // -------- Bubble Sort Input --------
        System.out.print("Enter number of elements for Bubble Sort: ");
        int n1 = sc.nextInt();

        int[] arr1 = new int[n1];
        System.out.println("Enter elements:");
        for (int i = 0; i < n1; i++) {
            arr1[i] = sc.nextInt();
        }

        Sortable ref = new BubbleSort();
        ref.sort(arr1);
        System.out.println("Array sorted using Bubble Sort:");
        printArray(arr1);

        // -------- Selection Sort Input --------
        System.out.print("Enter number of elements for Selection Sort: ");
        int n2 = sc.nextInt();

        int[] arr2 = new int[n2];
        System.out.println("Enter elements:");
        for (int i = 0; i < n2; i++) {
            arr2[i] = sc.nextInt();
        }

        ref = new SelectionSort();
        ref.sort(arr2);
        System.out.println("Array sorted using Selection Sort:");
        printArray(arr2);

        sc.close();
    }
}
```


## output:
![5a](https://github.com/user-attachments/assets/c5ff772f-bcad-4670-8ecc-5b1b5cc188ed)


# task 5b
## Aim:To write a JAVA program that implements Runtime polymorphism
```
 class vehicle {

    void run() {
        System.out.println("vehicle is running");
    }
}
 class car extends vehicle {

    @Override
    void run() {
        System.out.println("car is running on four wheels");
    }
}
 class bike extends vehicle {

    @Override
    void run() {
        System.out.println("bike is running on two wheels");
    }
}
 public class testvehicle {

    public static void main(String[] args) {

        vehicle v;   // base class reference

        v = new car();
        v.run();     // calls car's run()

        v = new bike();
        v.run();     // calls bike's run()

        v = new vehicle();
        v.run();     // calls vehicle's run()
    }
}
```
## output:
![5b](https://github.com/user-attachments/assets/737026d5-6b90-4bf4-9311-305370049336)

# task 5c
## Aim: To write a JAVA program using StringBuffer to delete, remove character.

```
public class StringBufferDelete {
    public static void main(String[] args) {

        // Create StringBuffer object
        StringBuffer sb = new StringBuffer("Java Programming");

        // Display original string
        System.out.println("Original String: " + sb);

        // Delete a single character at index 4
        sb.deleteCharAt(4);
        System.out.println("After deleting one character: " + sb);

        // Delete a range of characters from index 0 to 4
        sb.delete(0, 4);
        System.out.println("After deleting range of characters: " + sb);
    }
}
```
## output:
![5c](https://github.com/user-attachments/assets/f647eeaf-3f88-4306-b4f7-ac3b54c84c88)
