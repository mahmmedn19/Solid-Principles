**I will update this file from time to time while learning and adding updates. Thank you**

# SOLID Principles

This repository is an example project showcasing the **SOLID principles** of object-oriented software design. 

**The SOLID principles** are a set of guidelines that help to create maintainable, testable, and scalable code. These principles were first introduced **by Robert C. Martin** and they are:

- **Single Responsibility Principle:** A class should have one and only one reason to change, meaning that a class should have only one responsibility.

- **Open-Closed Principle:** A class should be open for extension but closed for modification, meaning that a class should be designed in a way that new functionality can be added without changing the existing code.

- **Liskov Substitution Principle:** A derived class should be able to replace its base class without affecting the correctness of the program.

- **Interface Segregation Principle:** A class should not be forced to implement interfaces it does not use.

- **Dependency Inversion Principle:** High-level modules should not depend on low-level modules, but both should depend on abstractions.

By following these principles, we can create software that is easy to ***understand, maintain, and extend.***

Each principle has its own specific meaning, and this project aims to provide examples for the implementation of these principles in various programming languages.

## Single Responsibility Principle (SRP)
**The Single Responsibility Principle** states that a class or module should have one, and only one, reason to change. In other words, a class or module should have a single, well-defined responsibility, and that responsibility should be encapsulated within the class or module. 


> here's an example of how the Single Responsibility Principle (SRP) can
> be violated, and then fixed, in a simple class called Employee in
> Kotlin:



### Violation of SRP
```kotlin
class Employee(var name: String, var address: String, var phone: String, var email: String) {

    fun saveToDatabase() {
        // code to save employee details to the database
    }

    fun validate(): Boolean {
        // code to validate employee's details
    }

    fun sendEmail() {
        // code to send email to employee
    }
}
```
**In this example, the Employee class is responsible for three different things: saving the employee's details to the database, validating the employee's details, and sending an email to the employee. This violates the Single Responsibility Principle because any change in one of the 3 concerns will affect the other, also making the code less testable.**

### Fixing SRP
```kotlin
class Employee(var name: String, var address: String, var phone: String, var email: String) {
    fun validate(): Boolean {
        // code to validate employee's details
    }
}
class EmployeeDatabaseRepository {
    fun save(employee: Employee) {
        // code to save employee details to the database
    }
}
class EmailService {
    fun send(employee: Employee) {
        // code to send email to employee
    }
}
```
**In this example, the concerns of the Employee class have been separated into different classes. The Employee class is only responsible for validating the employee's details, the EmployeeDatabaseRepository is responsible for saving the employee's details to the database, and the EmailService class is responsible for sending an email to the employee. This separation of concerns follows the Single Responsibility Principle, making the code more maintainable, testable and flexible.**


> It is important to note that this is only one way of applying the SRP
> and depending on the specifics of the application, the separation of
> responsibilities may vary.




This principle helps to keep the code more organized, making it easier to understand, modify, and test. For example, in this repository you will find examples of how to separate the concerns of a class and encapsulate them in different modules, classes or even new abstractions.


## HeadingInstallation :wrench:

In order to use the code in this repository, you will need to have a development environment set up on your machine. This will typically include a code editor, a JDK, and the necessary dependencies.

 1. Clone the repository **git clone** *https://github.com/mahmmedn19/Solid-Principles.git* 
 2. Import the project into your preferred development environment
 3.  Build and run the project

## HeadingContribute :handshake:

We welcome contributions to this repository. If you would like to contribute, please follow these steps:

## HeadingFork the repository

 1. Create a new branch for your feature or bug fix
 2.  Make your changes
 3. Create a pull request

## HeadingLicense :page_with_curl:

This project is licensed under the ***MoNaser*** License.

> Please feel free to customize these instructions as per your project
> requirements.
