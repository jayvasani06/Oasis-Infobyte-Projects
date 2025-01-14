import java.util.*;

class Bank {
    String Name;
    String UserName;
    String Password;
    float Balance = 0f;
    int Transactions = 0;
    String TranHistory = "";

    public void Register() {
        Scanner sc = new Scanner(System.in);
        System.out.println("******Welcome To Registration Portal******\n");
        System.out.print("Enter Name: ");
        Name = sc.nextLine();
        System.out.print("Enter UserName: ");
        UserName = sc.nextLine();
        System.out.print("Enter Password: ");
        Password = sc.nextLine();
        System.out.println("\nRegistration Successful!!");
    }

    public void Login() {
        Scanner sc = new Scanner(System.in);
        System.out.println("\n*******Enter Login Details******\n");
        System.out.print("Enter UserName: ");
        String username = sc.nextLine();
        if (username.equals(UserName)) {
            System.out.print("Enter Password: ");
            String password = sc.nextLine();
            if (password.equals(Password)) {
                System.out.print("\nYour Login Successfully!!!");
                return;
            } else {
                while (!password.equals(Password)) {
                    System.out.println("\nInvalid Password!!");
                    System.out.print("\nRe-Enter Password: ");
                    password = sc.nextLine();
                    if (password.equals(Password)) {
                        System.out.println("\nYour Login Successfully!!!");
                        return;
                    }
                }
            }
        } else {
            while(!username.equals(UserName)){
                System.out.println("Enter Valid Username");
                System.out.println("Re-Enter UserName");
                username = sc.nextLine();
                if(username.equals(UserName)){
                    System.out.print("Enter Password: ");
                    String password = sc.nextLine();
                    if (password.equals(Password)) {
                        System.out.print("\nYour Login Successfully!!!");
                        return;
                    } else {
                        while (!password.equals(Password)) {
                            System.out.println("\nInvalid Password!!");
                            System.out.print("\nRe-Enter Password: ");
                            password = sc.nextLine();
                            if (password.equals(Password)) {
                                System.out.println("\nYour Login Successfully!!!");
                                return;
                            }
                        }
                    }
                }

            }
        }
    }

    public void Deposite() {
        Scanner sc = new Scanner(System.in);
        System.out.print("\nEnter Value To Deposit Amount: ");
        float amt = sc.nextFloat();
        Balance += amt;
        Transactions++;
        System.out.println("\nCredit " + amt);
        TranHistory += "\nCredit " + amt;
        System.out.println("Your Balance Is: " + Balance);
        System.out.println("\nCredited Successfully!!!");
    }

    public void Withdraw() {
        Scanner sc = new Scanner(System.in);
        System.out.println("\nEnter Withdraw Amount: ");
        float amt = sc.nextFloat();
        if (amt > Balance) {
            System.out.println("\nInsufficient Balance!!");
        } else {
            Balance -= amt;
            Transactions++;
            System.out.println("\nDebit " + amt);
            System.out.println("Your Balance Is: " + Balance);
            TranHistory += "\nDebit " + amt;
            System.out.println("\nWithdraw Successfully!!!");
        }
    }

    public void TransHistory() {
        System.out.println("\nTransaction History");
        System.out.println("Your Transactions Are: " + Transactions);
        System.out.println(TranHistory);
    }

    public void Transfer() {
        Scanner sc = new Scanner(System.in);
        System.out.println("\nTransfer To Another Account");
        System.out.print("\nEnter Username: ");
        String name = sc.nextLine();
        System.out.print("\nEnter Transfer Amount: ");
        float amt = sc.nextFloat();
        if (amt > Balance) {
            System.out.println("\nInsufficient Balance!!");
        } else {
            Balance -= amt;
            System.out.println("\nDebit " + amt);
            TranHistory += "\nTransfer To " + name + " Amount: " + amt;
            Transactions++;
            System.out.println("Your Balance Is: " + Balance);
            System.out.println("\nTransfer Successfully!!!");
        }
    }
}

public class ATM {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Bank bank = new Bank();
        bank.Register();
        bank.Login();
        System.out.println("\n\n*******WELCOME TO DASHBOARD******");
        System.out.println("1. Transaction History");
        System.out.println("2. Withdraw");
        System.out.println("3. Deposit");
        System.out.println("4. Transfer");
        System.out.println("5. Exit");
        System.out.print("\nChoose Operation: ");
        int select = sc.nextInt();
        while (select != 5) {
            switch (select) {
                case 1:
                    bank.TransHistory();
                    break;
                case 2:
                    bank.Withdraw();
                    break;
                case 3:
                    bank.Deposite();
                    break;
                case 4:
                    bank.Transfer();
                    break;
                case 5:
                    return;
                default:
                    System.out.println("Enter Valid Number!!");
                    break;
            }
            System.out.println("\n\n*******WELCOME TO DASHBOARD******");
            System.out.println("1. Transaction History");
            System.out.println("2. Withdraw");
            System.out.println("3. Deposit");
            System.out.println("4. Transfer");
            System.out.println("5. Exit");
            System.out.print("\nChoose another option: ");
            select = sc.nextInt();
            sc.nextLine();
        }
        sc.close();
    }
}
