import java.util.ArrayList;
import java.util.Scanner;

class Transaction {
    String type;
    double amount;

    Transaction(String type, double amount) {
        this.type = type;
        this.amount = amount;
    }
}

public class ExpenseTracker {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Transaction> transactions = new ArrayList<>();
        double balance = 0;

        while (true) {
            System.out.println("\n1. Add Income\n2. Add Expense\n3. View Balance\n4. View All Transactions\n5. Exit");
            System.out.print("Choose an option: ");
            int choice = sc.nextInt();

            if (choice == 1) {
                System.out.print("Enter income amount: ");
                double amount = sc.nextDouble();
                transactions.add(new Transaction("Income", amount));
                balance += amount;
                System.out.println("Income added!");
            } else if (choice == 2) {
                System.out.print("Enter expense amount: ");
                double amount = sc.nextDouble();
                transactions.add(new Transaction("Expense", amount));
                balance -= amount;
                System.out.println("Expense added!");
            } else if (choice == 3) {
                System.out.println("Current Balance: " + balance);
            } else if (choice == 4) {
                System.out.println("\nAll Transactions:");
                for (Transaction t : transactions) {
                    System.out.println(t.type + ": " + t.amount);
                }
            } else if (choice == 5) {
                System.out.println("Exiting... Thank you!");
                break;
            } else {
                System.out.println("Invalid choice. Try again.");
            }
        }

        sc.close();
    }
}
