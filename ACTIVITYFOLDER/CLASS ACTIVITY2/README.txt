import java.util.*;

class Student {
    int id;
    String name;
    int marks;

    Student(int id, String name, int marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    void display() {
        System.out.println(id + " " + name + " " + marks);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ArrayList<Student> students = new ArrayList<>();

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            System.out.print("Enter ID: ");
            int id = sc.nextInt();

            System.out.print("Enter Name: ");
            String name = sc.next();

            System.out.print("Enter Marks: ");
            int marks = sc.nextInt();

            students.add(new Student(id, name, marks));
        }

        System.out.println("\nStudent Details");

        for (Student s : students) {
            s.display();
        }
    }
}
output
Enter number of students: 3
Enter ID: 1
Enter Name: kavya
Enter Marks: 55
Enter ID: 2
Enter Name: priya
Enter Marks: 89
Enter ID: 3
Enter Name: chandana
Enter Marks: 89

Student Details
1 kavya 55
2 priya 89
3 chandana 89

