# Day 09: Inheritance, Polymorphism & Employee Payroll Hierarchy

## 🎯 1. Goal of the Day
Implement an Employee base class with FullTimeEmployee and ContractEmployee subclasses demonstrating dynamic method dispatch.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day09;

public class PayrollEngine {
    public static abstract class Employee {
        private final String id;
        private final String name;
        public Employee(String id, String name) { this.id = id; this.name = name; }
        public String getId() { return id; }
        public String getName() { return name; }
        public abstract double calculatePay();
    }

    // TODO 9.1: Implement FullTimeEmployee (monthlySalary) extending Employee
    // TODO 9.2: Implement ContractEmployee (hourlyRate, hoursWorked) extending Employee
    // TODO 9.3: Polymorphic payroll processor looping over Employee[] array

    public static void main(String[] args) {
        System.out.println("Day 09 Payroll Hierarchy Challenge");
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Day 09 Payroll Hierarchy Challenge
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What is dynamic method dispatch?**
  - 💡 *Hint:* The mechanism by which a call to an overridden method is resolved at runtime rather than compile time.
- **Q2: Why should the `@Override` annotation always be used?**
  - 💡 *Hint:* It tells the compiler to verify that the method actually overrides a superclass or interface method, catching typo bugs.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day09): complete inheritance, polymorphism & employee payroll hierarchy"`.
