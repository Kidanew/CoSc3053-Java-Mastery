# Day 08: Interfaces, Abstract Classes & Contract-Driven Design

## 🎯 1. Goal of the Day
Design a Payable contract interface and an AbstractPaymentGateway base class for flexible payment processing.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day08;

public class PaymentGatewayDemo {

    public interface Payable {
        boolean processPayment(double amount);
        String getReceipt();
        default void logTrace(double amount) {
            System.out.println("[AUDIT] Processing payment: $" + amount);
        }
    }

    public static abstract class AbstractGateway implements Payable {
        private final String merchantId;
        public AbstractGateway(String merchantId) { this.merchantId = merchantId; }
        public String getMerchantId() { return merchantId; }
        public abstract double calculateFee(double amount);
    }

    // TODO 8.1: Implement CreditCardGateway extending AbstractGateway
    // TODO 8.2: Implement calculateFee(double amount) -> 2.5% fee
    // TODO 8.3: Implement processPayment(double amount) and getReceipt()

    public static void main(String[] args) {
        System.out.println("Day 08 Interfaces & Abstract Classes Challenge");
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Day 08 Interfaces & Abstract Classes Challenge
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: When should you choose an Abstract Class over an Interface?**
  - 💡 *Hint:* Use an Abstract Class when subtypes share state/fields or code implementation; use an Interface to define pure behavioral contracts.
- **Q2: What is a default method in a Java interface?**
  - 💡 *Hint:* A method with a default implementation in an interface (JDK 8+), allowing interface evolution without breaking existing implementations.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day08): complete interfaces, abstract classes & contract-driven design"`.
