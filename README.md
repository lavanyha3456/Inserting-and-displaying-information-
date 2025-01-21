# Inserting-and-displaying-information-
CODING:
import java.util.ArrayList;
import java.util.Scanner;
class Student {
// Fields
private int rollNumber;
private String name;
private double marks;
// Constructor
public Student(int rollNumber, String name, double marks) {
this.rollNumber = rollNumber;
this.name = name;
this.marks = marks;
}
// Method to display student details
public void displayDetails() {
System.out.println("Roll Number: " + rollNumber);
System.out.println("Name: " + name);
System.out.println("Marks: " + marks);
}
}
public class StudentDetails {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
ArrayList<Student> students = new ArrayList<>();
System.out.print("Enter the number of students: ");
int numberOfStudents = scanner.nextInt();
for (int i = 0; i < numberOfStudents; i++) {
System.out.println("\nEnter details for Student " + (i + 1) + ":");
System.out.print("Enter Roll Number: ");
int rollNumber = scanner.nextInt();
scanner.nextLine(); // Consume newline
System.out.print("Enter Name: ");
String name = scanner.nextLine();
System.out.print("Enter Marks: ");
double marks = scanner.nextDouble();
// Add student to the list
students.add(new Student(rollNumber, name, marks));
}
// Display all student details
System.out.println("\nStudent Details:");
for (int i = 0; i < students.size(); i++) {
System.out.println("\nStudent " + (i + 1) + ":");
students.get(i).displayDetails();
}
scanner.close();
}
}
OUTPUT:
Enter the number of students: 2
Enter details for Student 1:
Enter Roll Number: 101
Enter Name: Alice
Enter Marks: 88.5
Enter details for Student 2:
Enter Roll Number: 102
Enter Name: Bob
Enter Marks: 92.0
Student Details:
Student 1:
Roll Number: 101
Name: Alice
Marks: 88.5
Student 2:
Roll Number: 102
Name: Bob
Marks: 92.0
