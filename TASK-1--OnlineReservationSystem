import java.util.HashMap;
import java.util.Scanner;

public class Main {
    private static HashMap<String, String> users = new HashMap<>();
    private static HashMap<Integer, Ticket> tickets = new HashMap<>();
    private static int pnrCounter = 1001;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        users.put("admin", "admin@123");

        System.out.println("Welcome to the Online Reservation System!");
        boolean loggedIn = false;

        while (!loggedIn) {
            System.out.print("Enter Login ID: ");
            String loginId = scanner.nextLine();
            System.out.print("Enter Password: ");
            String password = scanner.nextLine();

            if (users.containsKey(loginId) && users.get(loginId).equals(password)) {
                loggedIn = true;
                System.out.println("Login successful!");
            } else {
                System.out.println("Invalid Login ID or Password. Try again.");
            }
        }

        boolean exit = false;
        while (!exit) {
            System.out.println("\nMenu:");
            System.out.println("1. Reserve Ticket");
            System.out.println("2. Cancel Ticket");
            System.out.println("3. View All Tickets");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();
            scanner.nextLine();

            switch (choice) {
                case 1:
                    reserveTicket(scanner);
                    break;
                case 2:
                    cancelTicket(scanner);
                    break;
                case 3:
                    viewTickets();
                    break;
                case 4:
                    exit = true;
                    System.out.println("Exiting the system. Goodbye!");
                    break;
                default:
                    System.out.println("Invalid choice. Try again.");
            }
        }

        scanner.close();
    }

    private static void reserveTicket(Scanner scanner) {
        System.out.print("Enter Your Name: ");
        String name = scanner.nextLine();
        System.out.print("Enter Train Number: ");
        int trainNumber = scanner.nextInt();
        scanner.nextLine();
        System.out.print("Enter Train Name: ");
        String trainName = scanner.nextLine();
        System.out.print("Enter Class Type (e.g., AC, Sleeper): ");
        String classType = scanner.nextLine();
        System.out.print("Enter Date of Journey (YYYY-MM-DD): ");
        String date = scanner.nextLine();
        System.out.print("Enter From (Place): ");
        String from = scanner.nextLine();
        System.out.print("Enter To (Destination): ");
        String to = scanner.nextLine();

        Ticket ticket = new Ticket(pnrCounter, name, trainNumber, trainName, classType, date, from, to);
        tickets.put(pnrCounter, ticket);
        System.out.println("Ticket Reserved Successfully! Your PNR is: " + pnrCounter);
        pnrCounter++;
    }

    private static void cancelTicket(Scanner scanner) {
        System.out.print("Enter PNR Number to Cancel: ");
        int pnr = scanner.nextInt();
        scanner.nextLine();

        if (tickets.containsKey(pnr)) {
            Ticket ticket = tickets.get(pnr);
            System.out.println("Ticket Details: " + ticket);
            System.out.print("Are you sure you want to cancel this ticket? (yes/no): ");
            String confirmation = scanner.nextLine();

            if (confirmation.equalsIgnoreCase("yes")) {
                tickets.remove(pnr);
                System.out.println("Ticket Cancelled Successfully.");
            } else {
                System.out.println("Cancellation Aborted.");
            }
        } else {
            System.out.println("PNR Not Found.");
        }
    }

    private static void viewTickets() {
        if (tickets.isEmpty()) {
            System.out.println("No Tickets Reserved.");
        } else {
            System.out.println("All Reserved Tickets:");
            for (Ticket ticket : tickets.values()) {
                System.out.println(ticket);
            }
        }
    }
}

class Ticket {
    private int pnr;
    private String name;
    private int trainNumber;
    private String trainName;
    private String classType;
    private String date;
    private String from;
    private String to;

    public Ticket(int pnr, String name, int trainNumber, String trainName, String classType, String date, String from, String to) {
        this.pnr = pnr;
        this.name = name;
        this.trainNumber = trainNumber;
        this.trainName = trainName;
        this.classType = classType;
        this.date = date;
        this.from = from;
        this.to = to;
    }

    @Override
    public String toString() {
        return "PNR: " + pnr +
                ", Name: " + name +
                ", Train Number: " + trainNumber +
                ", Train Name: " + trainName +
                ", Class Type: " + classType +
                ", Date: " + date +
                ", From: " + from +
                ", To: " + to;
    }
}
