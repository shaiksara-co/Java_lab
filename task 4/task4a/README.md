# Experiment 4a
## AIM: To write a JAVA program to implement Single Inheritance.
```
java
// Person.java
public class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display person details
    void displayPersonDetails() {
        System.out.println("Name : " + name);
        System.out.println("Age  : " + age);
    }
}



// Employee.java
public class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    // Constructor
    Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
        super(name, age); // calling Person class constructor
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    // Method to display employee details
    void displayEmployeeDetails() {
        displayPersonDetails(); // inherited method
        System.out.println("Annual Salary : " + annualSalary);
        System.out.println("Year of Joining : " + yearOfJoining);
        System.out.println("National Insurance Number : " + nationalInsuranceNumber);
    }
}


// TestEmployee.java
public class TestEmployee {
    public static void main(String[] args) {

        Employee emp1 = new Employee(
                "Sai Karthik",
                22,
                450000.00,
                2024,
                "NIN12345"
        );

        emp1.displayEmployeeDetails();
    }
}
```

## output:
![java4a](https://github.com/user-attachments/assets/3e974b2c-4788-4bf7-a0ec-d26fc78d3497)

