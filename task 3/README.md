## task 3
# task 3a
## TITLE implement conctructor overloading in java
```
class Student {

	String name;
	int age;
	double marks;

	Student() {

	}

	Student(String name, int age, double marks) {

		this.name=name;
		this.age=age;
		this.marks=marks;

	}

	void display() {

		System.out.println("Name: "+name);
		System.out.println("Age: "+age);
		System.out.println("marks: "+marks);

	}

}
class Main {

	public static void main(String args[]) {

		Student std = new Student();
		std.display();

		Student std1 = new Student("Hari", 40, 67.8);
		std1.display();

	}
}
```
# OUTPUT
![task 3a 5as](https://github.com/user-attachments/assets/54fbbc6d-7a76-41eb-975a-b79386b7bc0e)

# task 3b
## TITLE implement binary search in java
```
import java.util.Scanner;
import java.util.Arrays;

class BinarySearch {

    int list[];
    int size;
    int key = -1;

    BinarySearch(int size) {
        this.size = size;
        list = new int[size];
    }

    void set_list() {
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i < list.length; i++) {
            list[i] = sc.nextInt();
        }
    }

    void get_list() {
        for (int i = 0; i < list.length; i++) {
            System.out.print(list[i] + " ");
        }
        System.out.println();
    }

    int binarysearch(int key) {
        int low = 0;
        int high = list.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (list[mid] == key) {
                return mid;
            } else if (list[mid] < key) {
                low = mid + 1;
            } else {
                high = mid - 1;
            }
        }
        return -1;
    }

    void getItem(int index) {
        System.out.println("Key element is found at index " + index);
        System.out.println("Key element is " + list[index]);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size: ");
        int size = sc.nextInt();

        BinarySearch s = new BinarySearch(size);

        System.out.println("Enter elements:");
        s.set_list();

        Arrays.sort(s.list);   // IMPORTANT for binary search

        System.out.println("Sorted list:");
        s.get_list();

        System.out.print("Enter key to search: ");
        int key = sc.nextInt();

        int index = s.binarysearch(key);

        if (index != -1) {
            s.getItem(index);
        } else {
            System.out.println("Key element not found");
        }
    }
}
```
# OUTPUT
![task 3b 5as](https://github.com/user-attachments/assets/a0646595-2a60-4e0c-9052-113490f3a446)

