Exception Handling Demo

This project demonstrates the basics of exception handling in programming using a try–catch–finally block. It is designed to help beginners understand how exceptions occur, how they can be caught, and how cleanup code can be executed regardless of whether an exception happens.

📌 Features

Shows how to wrap risky code in a try block

Demonstrates how to handle errors with one or more catch blocks

Uses a finally block to execute cleanup or mandatory code

Provides clear console output to understand the control flow

Helps new developers learn robust error-handling techniques

📂 File Structure
project/
│── src/
│     └── ExceptionDemo.java (or .py, .cs, etc.)
└── README.md

💡 How It Works

The program attempts to execute code that may throw an exception—such as dividing by zero or parsing invalid input.

If an exception occurs, control is passed to the catch block, where the error is handled gracefully.

Regardless of whether an exception is thrown, the finally block executes. Common uses include:

Releasing resources (files, database connections)

Logging

Cleanup tasks

🧪 Example (Java)
public class ExceptionDemo {
    public static void main(String[] args) {
        try {
            int a = 10;
            int b = 0;
            int result = a / b; // This will throw ArithmeticException
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Cannot divide by zero!");
        } catch (Exception e) {
            System.out.println("An unexpected error occurred: " + e.getMessage());
        } finally {
            System.out.println("Execution completed (finally block).");
        }
    }
}

▶️ Running the Program

Compile and run (example for Java):

javac ExceptionDemo.java
java ExceptionDemo


Expected Output:

Error: Cannot divide by zero!
Execution completed (finally block).
