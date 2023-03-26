# Encapsulation

Encapsulation is a fundamental concept in object-oriented programming that involves the hiding of the internal details of an object and providing access to it through public methods. Here's an example of encapsulation in Java:

```
public class BankAccount {
    private String accountNumber;
    private double balance;
    
    public BankAccount(String accountNumber, double balance) {
        this.accountNumber = accountNumber;
        this.balance = balance;
    }
    
    public void deposit(double amount) {
        balance += amount;
    }
    
    public void withdraw(double amount) {
        if (balance < amount) {
            System.out.println("Insufficient funds.");
        } else {
            balance -= amount;
        }
    }
    
    public double getBalance() {
        return balance;
    }
}
```

In this example, we have defined a BankAccount class that has two private instance variables accountNumber and balance. These variables are hidden from the outside world and can only be accessed through the public methods deposit, withdraw, and getBalance.

The deposit method takes in a double value and adds it to the balance variable. The withdraw method takes in a double value and checks if the balance variable is greater than or equal to the amount to be withdrawn. If the balance is less than the amount to be withdrawn, it displays an error message; otherwise, it subtracts the amount from the balance variable.

The getBalance method returns the current value of the balance variable, which can be accessed by other objects outside the BankAccount class.

By using encapsulation, we are able to hide the internal details of the BankAccount class from the outside world and provide a secure way to access and modify its properties through the public methods. This helps to prevent unintended modifications of the balance variable and ensures that the behavior of the class remains consistent and predictable.