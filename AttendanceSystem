import java.util.Scanner;

class Student {
    String rollNo;
    String name;
    boolean isPresent;

    Student(String rollNo, String name) {
        this.rollNo = rollNo;
        this.name = name;
        this.isPresent = false; // default absent
    }
}

public class AttendanceSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Sample students
        Student[] students = {
            new Student("101", "Aarav Sharma"),
            new Student("102", "Isha Patel"),
            new Student("103", "Rohit Kumar"),
            new Student("104", "Neha Gupta")
        };

        System.out.println("=== Student Attendance System ===");
        for (Student s : students) {
            System.out.print("Mark attendance for " + s.rollNo + " - " + s.name + " (P/A): ");
            char choice = sc.next().toUpperCase().charAt(0);
            if (choice == 'P') {
                s.isPresent = true;
            }
        }

        System.out.println("\n--- Attendance Report ---");
        int presentCount = 0, absentCount = 0;
        for (Student s : students) {
            String status = s.isPresent ? "Present" : "Absent";
            System.out.println(s.rollNo + " - " + s.name + " : " + status);
            if (s.isPresent) presentCount++;
            else absentCount++;
        }

        System.out.println("\nTotal Students: " + students.length);
        System.out.println("Present: " + presentCount);
        System.out.println("Absent: " + absentCount);

        sc.close();
    }
}
