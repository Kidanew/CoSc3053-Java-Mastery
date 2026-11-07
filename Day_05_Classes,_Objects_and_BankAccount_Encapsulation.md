# Day 05: Classes, Objects & BankAccount Encapsulation

## 🎯 1. Goal of the Day
Create an encapsulated BankAccount class with state invariants, deposit, and withdraw methods.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day05;

public class BankAccount {
    // TODO 5.1: Declare private encapsulated fields
    // - accountNumber (String, read-only)
    // - accountHolder (String)
    // - balance (double)
    // - MINIMUM_BALANCE = 25.00 (static final double)

    // TODO 5.2: Implement 3-arg constructor with defensive validation
    // HINT: Check accountNumber != null && !accountNumber.isBlank(); initialDeposit >= 25.00

    // TODO 5.3: Implement deposit(double amount) -> return boolean success
    // HINT: Ensure amount > 0.0 before updating balance.

    // TODO 5.4: Implement withdraw(double amount) -> return boolean success
    // HINT: Ensure amount > 0.0 AND (balance - amount) >= MINIMUM_BALANCE ($25.00).

    public static void main(String[] args) {
        BankAccount acc = new BankAccount("ACC-101", "Abebe Bekele", 500.00);
        acc.deposit(150.00);
        acc.withdraw(100.00);
        acc.withdraw(600.00); // Should fail minimum balance check ($25.00)
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
✅ [SUCCESS] Deposited $150.00 -> New Balance: $650.00
✅ [SUCCESS] Withdrew $100.00 -> New Balance: $550.00
❌ [REJECTED] Withdrawal of $600.00 denied: Remaining balance ($50.00) would fall below $25.00 minimum balance requirement.
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why should `balance` not have a public `setBalance(double b)` method?**
  - 💡 *Hint:* A setter bypasses validation logic and allows external code to set arbitrary or invalid balance states.
- **Q2: What is the benefit of declaring `accountNumber` as `final`?**
  - 💡 *Hint:* It makes the account ID immutable once initialized by the constructor.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day05): complete classes, objects & bankaccount encapsulation"`.
