# Kotlin

## What is Kotlin?
Kotlin is a general-purpose, free, open-source, statically typed programming language initially designed for the JVM (Java Virtual Machine) and Android. It combines object-oriented and functional programming features.

## Where is Kotlin used?
Kotlin is designed to run on a Java Virtual Machine and can run side by side with Java. Although Kotlin first started as a language for Android development specifically, it quickly spread through the Java community because of its features and has since been used for many types of applications. It is used in the following areas:
- Android Development
- Backend Development
- Full Stack Development
- Multi-Platform Mobile Development

## Features of Kotlin
- Data Classes
- Concise
- Null Safety
- Interoperable with Java
- Functional and OOP Capabilities
- Smart Cast
- Tool-Friendly

## First Program Using Kotlin
- Online Compiler: [https://play.kotlinlang.org/](https://play.kotlinlang.org/)
- Environment Setup on Windows: [https://www.tutorialspoint.com/kotlin/kotlin_environment_setup.htm](https://www.tutorialspoint.com/kotlin/kotlin_environment_setup.htm)
- Environment Setup on Local Machine (Linux):
  - Update apt to load the latest package on apt:
    ```
    sudo su
    apt update
    ```
  - Install JDK and JRE:
    ```
    apt install default-jre
    apt install default-jdk
    ```
  - Install SDKMAN:
    ```
    curl -s "https://get.sdkman.io" | bash
    source "/root/.sdkman/bin/sdkman-init.sh"
    ```
  - Install Kotlin:
    ```
    sdk install kotlin
    ```

 - Code
    - Create a demo Kotlin file and save it with the name `hello.kt` in any IDE you want:

    ```kotlin
    fun main() {
        println("Hello World!")
    }
    
 - Execution
    - Run the below mentioned command for creating jar file with mentioned name 

    ```bash
    kotlinc hello.kt -include-runtime -d hello.jar
    ```


    - Now executing jar file with java command as mentioned below.

    ```bash
    java -jar hello.jar
    ```
## Scan
 - Kotlin uses java.util.Scanner class to scan user inputs.
 - To read a string, nextLine() method is used.
 - Similarly, it has methods like nextInt(), nextLong() methods to get inputs of corresponding types.
| Code |
|------|
| ```kotlin
    import java.util.Scanner

    fun main() {

       val scanner = Scanner(System.`in`)
       val num1 = scanner.nextInt()
       println("The input one is : $num1")
       val num2 = scanner.nextInt()
       println("The input two is : $num2")

       val sum = num1 + num2

       println("The sum of the two inputs is : $sum")
    }|
 
## Conditions and Loops
## Returns and Jumps
## Kotlin Collections
## Functions
## OOP Concepts
## Null Safety
## Kotlin v/s Java for Android Development
## Courses

