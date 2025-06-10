import java.util.Scanner;

class  Task2StudentsGradeCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("ENTER HOW MANY SUBJECTS?");
        int n = sc.nextInt();

        int[] marks = new int[n];
        int total = 0;
        float averagePer;
        String grade;

        System.out.println("ENTER MARKS FOR " + n + " SUBJECTS (OUT OF 100):");

        for (int i = 0; i < n; i++) {
            System.out.print("ENTER MARKS FOR SUBJECT " + (i + 1) + ": ");
            marks[i] = sc.nextInt();
            total += marks[i];
        }

        averagePer = total / (float) n;

        if (averagePer > 90 && averagePer <= 100) {
            grade = "A+";
        } else if (averagePer >= 80 && averagePer <= 90) {
            grade = "A";
        } else if (averagePer >= 70 && averagePer < 80) {
            grade = "B";
        } else if (averagePer >= 60 && averagePer < 70) {
            grade = "C";
        } else if (averagePer >= 50 && averagePer < 60) {
            grade = "D";
        } else if (averagePer >= 40 && averagePer < 50) {
            grade = "E";
        } else {
            grade = "FAIL";
        }

        System.out.printf("TOTAL MARKS: %d\nAVERAGE PERCENTAGE: %.2f\nGRADE: %s", total, averagePer, grade);

        sc.close();
    }
}

