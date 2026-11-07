# Day 01: JDK 25 Setup & Environment Diagnostic

## 🎯 1. Goal of the Day
Set up Temurin JDK 25 and write an environment diagnostic program that outputs system properties.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day01;

public class EnvironmentDiagnostic {
    public static void main(String[] args) {
        // TODO 1.1: Print a welcoming header message
        // HINT: System.out.println("=== HARAMAYA CS: DAY 01 ===");

        // TODO 1.2: Retrieve and print "java.version" property
        // HINT: String javaVer = System.getProperty("java.version");

        // TODO 1.3: Retrieve and print "os.name" and "os.arch" properties
        // HINT: System.getProperty("os.name");

        // TODO 1.4: Retrieve and print "user.name" property
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
=== HARAMAYA CS: DAY 01 ===
Java Version : 25.0.1
OS Name      : Linux
OS Arch      : amd64
User Name    : HaramayaStudent
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: How do you verify your installed JDK version from the terminal?**
  - 💡 *Hint:* Run `java -version` and `javac -version` in Command Prompt / Terminal.
- **Q2: What is the role of JAVA_HOME?**
  - 💡 *Hint:* It tells build tools (Maven, Gradle, IDEs) where the JDK installation root is located.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day01): complete jdk 25 setup & environment diagnostic"`.
