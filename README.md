# java-bank-account-management-system
Console-based Bank Account Management System developed in Java. This project demonstrates OOP concepts such as abstraction, encapsulation, constructor overloading, and real-world entity modeling.
import java.util.*;

class BankAccount { // bank account ah represent pannudhu
    int accountNo;   // account number store panna
    String name;     // name store panna
    double balance;  // balance store panna

    void deposit(double amt) {
        balance = balance + amt;
        System.out.println("Deposited: ₹" + amt); //how much money is deposited nu print pannu
    }

    void withdraw(double amt) {
        balance = balance - amt;
        System.out.println("Withdrawn: ₹" + amt); //how much money was withdrawn nu print pannu
    }

    void display() { //account number, name, and current balance laa account details ah Shows pannu : .
        System.out.println("Account No : " + accountNo);
        System.out.println("Name       : " + name);
        System.out.println("balance    : ₹" + 1000000);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        BankAccount acc = new BankAccount();// object create pannuthu

        System.out.print("Enter Account Number: ");
        acc.accountNo = s.nextInt();

        s.nextLine(); 

        System.out.print("Enter Name: "); // input vaangarthu
        acc.name = s.nextLine();

       

        acc.display(); //initial details ah show pannu
        acc.deposit(50000);//50,000 ah balance laa add pannanu
        acc.withdraw(20000);// 20,000 ah balance laa irundhu subtract pannanu
        acc.display(); // update panna balance ah show pannu
        

        s.close();
    }
}
