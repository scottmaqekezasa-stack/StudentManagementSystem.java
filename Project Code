import java.util.ArrayList;
import java.util.Scanner;

// Student Management System - Sanlam Fintech Portfolio
// Author: Lisakhanya Maqekeza - NQF 5 ICT App Dev (5 Distinctions)
// Skills: Java, OOP, CRUD, Data Management

class Student {
    String id, name, course;
    int age;
    Student(String id, String name, String course, int age){
        this.id = id; this.name = name; this.course = course; this.age = age;
    }
    public String toString(){
        return id + " | " + name + " | " + course + " | Age: " + age;
    }
}

public class StudentManagementSystem {
    static ArrayList<Student> students = new ArrayList<>();
    static Scanner sc = new Scanner(System.in);

    public static void main(String[] args){
        // Sample data - demonstrates database logic
        students.add(new Student("S2023001", "Lisakhanya M", "ICT App Dev", 24));
        students.add(new Student("S2023002", "Test Student", "Information Systems", 22));

        int choice;
        do {
            System.out.println("\n--- SANLAM FINTECH STUDENT MANAGER ---");
            System.out.println("1. Add Student\n2. View All\n3. Search by ID\n4. Delete\n5. Exit");
            System.out.print("Choose: ");
            choice = sc.nextInt(); sc.nextLine();
            switch(choice){
                case 1: addStudent(); break;
                case 2: viewAll(); break;
                case 3: search(); break;
                case 4: delete(); break;
            }
        } while(choice !=5);
    }

    static void addStudent(){
        System.out.print("ID: "); String id = sc.nextLine();
        System.out.print("Name: "); String name = sc.nextLine();
        System.out.print("Course: "); String course = sc.nextLine();
        System.out.print("Age: "); int age = sc.nextInt(); sc.nextLine();
        students.add(new Student(id,name,course,age));
        System.out.println("Student added successfully!");
    }
    static void viewAll(){
        System.out.println("\n--- All Students ---");
        for(Student s: students) System.out.println(s);
    }
    static void search(){
        System.out.print("Enter ID to search: "); String id = sc.nextLine();
        for(Student s: students) if(s.id.equals(id)) System.out.println("Found: " + s);
    }
    static void delete(){
        System.out.print("Enter ID to delete: "); String id = sc.nextLine();
        students.removeIf(s -> s.id.equals(id));
        System.out.println("Deleted if existed.");
    }
}
