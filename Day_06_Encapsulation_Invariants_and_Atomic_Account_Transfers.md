# Day 06: Encapsulation Invariants & Atomic Account Transfers

## 🎯 1. Goal of the Day
Implement an atomic transfer service between BankAccount instances with validation and rollback guards.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day06;

public class BankAccountTransfer {
    // BankAccount class from Day 5 assumed available

    // TODO 6.1: Implement static transfer(BankAccount src, BankAccount dest, double amount)
    // HINT: Validate src != null, dest != null, src != dest, amount > 0.0.
    // HINT: Attempt src.withdraw(amount). If successful, dest.deposit(amount) and return true.
    public static boolean transfer(BankAccount src, BankAccount dest, double amount) {
        return false; // Replace
    }

    public static void main(String[] args) {
        BankAccount acc1 = new BankAccount("ACC-101", "Abebe", 500.0);
        BankAccount acc2 = new BankAccount("ACC-102", "Kebede", 200.0);

        boolean success = transfer(acc1, acc2, 150.0);
        System.out.println("Transfer Success: " + success);
        System.out.println("ACC-101 Balance: $" + acc1.getBalance());
        System.out.println("ACC-102 Balance: $" + acc2.getBalance());
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Transfer Success: true
ACC-101 Balance: $350.0
ACC-102 Balance: $350.0
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What is transfer atomicity?**
  - 💡 *Hint:* It guarantees that either both withdrawal and deposit succeed, or neither occurs, preventing money creation or loss.
- **Q2: Why guard against self-transfers (`src == dest`)?**
  - 💡 *Hint:* Self-transfers can cause redundant operations or unexpected balance calculations.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day06): complete encapsulation invariants & atomic account transfers"`.
