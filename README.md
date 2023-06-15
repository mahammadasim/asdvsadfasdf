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
    ```
    
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

    ```kotlin
    import java.util.Scanner

    fun main() {
        val scanner = Scanner(System.`in`)
        val num1 = scanner.nextInt()
        println("The input one is: $num1")
        val num2 = scanner.nextInt()
        println("The input two is: $num2")

        val sum = num1 + num2

        println("The sum of the two inputs is: $sum")
    }
    ```
    **Output** 
    ```
    Enter the inputs for addition
    10
    The input one is : 10
    100
    The input two is : 100
    The sum of the two inputs is : 110 
    ```


## Conditions and Loops
### if-else
  - If-else statement in Kotlin is similar to other programming languages such as C, C++, Java, and C#. However, in Kotlin, it also returns a value.
  - Kotlin eliminates the need for a ternary operator.

  ```kotlin
  // Only if
  if (a < b) {
      // Conditional logic for if
  }

  // if-else 
  if (a > b) {
      // Conditional logic for if
  } else {
      // Conditional logic for else
  }

  // As expression
  val max = if (a > b) a else b

  // if expression with blocks and return values
  val max = if (a > b) {
      print("Choose a")
      a
  } else {
      print("Choose b")
      b
  }
  ```

<h3> Reference </h3>

- [Kotlin if Expression](https://www.javatpoint.com/kotlin-if-expression)

### when
- It is a conditional expression with multiple branches. It is same as switch statement in other languages in C, C++, Java, C#.
    - We can use when statement in 2 ways

        1. With Expression

            ```kotlin
            fun main() {  
                var number = 4  
                var numberProvided = when (number) {  
                    1 -> "One"  
                    2 -> "Two"  
                    3 -> "Three"  
                    4 -> "Four"  
                    5 -> "Five"  
                    else -> "Invalid number"  
                }  
                println("You provided: $numberProvided")  
            }
            ```
            [[Try it Yourself](http://jdoodle.com/ia/IGy)]
            
        2. Without Expression
    
            ```kotlin
            fun main(){  
  
                var number = 4  
                when(number) {  
                    1 -> println("One")  
                    2 -> println("Two")  
                    3 -> println("Three")  
                    4 -> println("Four")  
                    5 -> println("Five")  
                    else -> println("invalid number")  
                }  
              
            }
            ```
            [[Try it Yourself](http://jdoodle.com/ia/IGz)]

            
<h3> Reference </h3>

- [Kotlin when Expression](https://www.javatpoint.com/kotlin-when-expression)

### for loop
- Scanning the integer value by using for loop.

    ```kotlin
    import java.util.Scanner
    fun main(){
       val scanner = Scanner(System.`in`)
       val n = scanner.nextInt()
       val a = arrayOfNulls<Int>(n);
       for(i in 0..n-1){
           a[i] = scanner.nextInt();
       }
       for(x in a){
           println(x);
       }
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGB)]
    
- Printing each element of array by iterator without using 

    ```kotlin
    fun main() {  
        val marks = arrayOf(80,85,60,90,70)  
        for(item in marks)  
            println(item)  
    }  
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGC)]

- Printing element using indexes 

    ```kotlin
    fun main(args : Array<String>) {  
     
        val marks = arrayOf(80,85,60,90,70)  
        for(item in marks.indices)  
           println("marks[$item]: "+ marks[item])  
    }
    ```  
    [[Try it Yourself](http://jdoodle.com/ia/IGD)]

- Different types of for loops with iterating loop in range

    ```kotlin
    fun main() {  
  
        print("for (i in 1..5) print(i) = ")  
        for (i in 1..5) print(i)  
        println()  
    
        print("for (i in 5..1) print(i) = ")  
        for (i in 5..1) print(i)    // prints nothing  
        println()  
    
        print("for (i in 5 downTo 1) print(i) = ")  
        for (i in 5 downTo 1) print(i)  
        println()  
    
        print("for (i in 5 downTo 2) print(i) = ")  
        for (i in 5 downTo 2) print(i)  
        println()  
    
        print("for (i in 1..5 step 2) print(i) = ")  
        for (i in 1..5 step 2) print(i)  
        println()  
        
        print("for (i in 5 downTo 1 step 2) print(i) = ")  
        for (i in 5 downTo 1 step 2) print(i)  
    }  
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGF)]

    **Output**
    ```
    for (i in 1..5) print(i) = 12345
    for (i in 5..1) print(i) = 
    for (i in 5 downTo 1) print(i) = 54321
    for (i in 5 downTo 2) print(i) = 5432
    for (i in 1..5 step 2) print(i) = 135
    for (i in 5 downTo 1 step 2) print(i) = 531
    ```

<h3> Reference </h3>

- [Kotlin for Loop](https://www.javatpoint.com/kotlin-for-loop)

### while and do-while loop
- while checks the condition and, if it's satisfied, executes the body and then returns to the condition check.
- do-while executes the body and then checks the condition. If it's satisfied, the loop repeats. So, the body of do-while executes at least once regardless of the condition.

    ```kotlin
    fun main() {  
      
        var i = 1  
        while (i<=5){  
            println(i)  
            i++  
        }
    
        println("\nDo While")  
        do {  
            println(i)  
            i--
        }  
        while (i>=0);  
    } 
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGG)]


<h3> References </h3>

- [Kotlin while Loop](https://www.javatpoint.com/kotlin-while-loop)
- [Kotlin do-while Loop](https://www.javatpoint.com/kotlin-do-while-loop)

## Returns and Jumps
### break
- **break**
    - A `break` expression is used to terminate the nearest enclosing loop. It is almost used with if-else conditions.
    ```kotlin
    for(..){  
        //body of for  
        if(checkCondition){  
            break;  
        }  
    }  
    ```
- **labled break**
    - Kotlin `labeled break` expression is used to terminate the specific loop. This is done by using the break expression with @ sign followed by label name (break@loop).

    ```kotlin
    fun main() {  
        loop@ for (i in 1..3) {  
            for (j in 1..3) {  
                println("i = $i and j = $j")  
                if (i == 2)  
                    break@loop  
            }  
        }  
    }  
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGH)]

    **Output**
    ```
    i = 1 and j = 1
    i = 1 and j = 2
    i = 1 and j = 3
    i = 2 and j = 1
    ```
### continue
- **continue**
    - `continue` statement is used to repeat the loop. It continues the current flow of the program and skips the remaining code at specified condition.
    ```kotlin
    for(..){  
        //body of for above if  
        if(checkCondition){  
            continue  
        }  
    //body of for below if  
    }  
    ```
- **labled continue**
    - `labeled continue` is used to skip the iteration of the desired block when it satisfies a specific condition without checking the condition in the while loop. If you mark the outer loop using the label outer@ and inner loop using inner@ then you can easily skip for the specific condition using continue@outer in the conditional block.

    ```kotlin
    fun main() {
        var num1 = 4
        outer@ while (num1 > 0) {
            num1--
            var num2 = 4
            println("1 num1 = $num1, num2 = $num2")
            inner@ while (num2 > 0) {
                if (num1 <= 2)
                    continue@outer
                println("2 num1 = $num1, num2 = $num2")
                num2--
            }
        }
    }   
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGJ)]

    **Output**
    ```
    1 num1 = 3, num2 = 4
    2 num1 = 3, num2 = 4
    2 num1 = 3, num2 = 3
    2 num1 = 3, num2 = 2
    2 num1 = 3, num2 = 1
    1 num1 = 2, num2 = 4
    1 num1 = 1, num2 = 4
    1 num1 = 0, num2 = 4
    ```
### return
- functions can be nested using function literals, local functions, and object expressions. Qualified return allows us to return from an outer function. The most important use case is returning from a lambda expression.

    ```kotlin
    fun main() {
        listOf(1, 2, 3, 4, 5).forEach {
            if (it == 3) return
            print(it)
        }
        println("this point is unreachable")
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGK)]
    
    **Output**
    ```
    12
    ```

<h3> References </h3>

- [Returns, Jumps and Labels in Kotlin](https://www.geeksforgeeks.org/returns-jumps-and-labels-in-kotlin/) (GFG)
- [Returns and jumps](https://kotlinlang.org/docs/returns.html) (Kotlin ORG)
- [Kotlin Return and Jump](https://www.javatpoint.com/kotlin-return-and-jump) (JavaTPoint)


## Kotlin Collections
### listOf()
- Kotlin List is an interface and generic collection of elements. The List interface inherits form Collection`<T>` class. It is immutable and its methods support only read functionalities.
### mutableListOf()
- Kotlin MutableList is an interface and generic collection of elements. MutableList interface is mutable in nature. The methods of MutableList interface supports both read and write functionalities. Once the elements in MutableList have been declared, it can be added more elements in it or removed, so it has no fixed size length.
### arrayListOf()
- An arrayListOf() is a function of the ArrayList class. ArrayList is mutable which means it provides both read am write functionalities. The arrayListOf() function returns an ArrayList type.
### mapOf()
- Kotlin Map is an interface and generic collection of elements. Map interface holds data in the form of key and value pair. Map key are unique and hold only one value for each key. The key and value may be of different pairs such as <Int, Int>,<Int, String>, <Char, String>etc. This interface is immutable, fixed size and its methods support read only access.
### hashMapOf()
- Kotlin HashMap is a class of collection based on the MutableMap interface. Kotlin HashMap class implements the MutableMap interface using Hash table. It stores the data in the form of key and value pairs. It is represented as HashMap<key, value> or HashMap<K, V>.
- The implementation of HashMap class does not make guarantees about the order of data of key, value and entries of collections.
- A hashMapOf() is a function of the HashMap class. It returns a new HashMap with the specified contents. It contains pairs of data in the form of key and value. HashMap is a mutable collection which provides both read and write functionalities.
### mutableMapOf()
- Kotlin MutableMap is an interface of collection framework that holds the object in the form of key and value pair. The values of the MutableMap interface are retrieved by using their corresponding keys. The key and value may be of different pairs such as <Int, Int>,<Int, String>, <Char, String> etc. Each key of MutableMap holds only one value.
- To use the MutableMap interface we need to use its function called mutableMapOf() or mutableMapOf <k,v>().
### setOf()
- Kotlin Set interface is a generic unordered collection of elements. Set interface does not support duplicate elements. This interface is immutable in nature; its methods support read-only functionality of the set.
- Set interface uses setOf() function to create the list of objects of the set interface which contains a list of elements.
### mutableSetOf()
- Kotlin MutableSet interface is a generic unordered collection of elements. MutableSet interface does not support duplicate elements. This interface is mutable so its methods support read-write functionality that supports adding and removing elements.
- Set interface uses mutableSetOf() function to create the list of objects of set interface which contains a list of elements.
### hashSetOf()
- Kotlin HashSet is a collection class which extends AbstractMutableSet class and implements Set interface. The HashSet class stores elements using a hashing mechanism. - It supports both read and write functionality. It does not support duplicate value and does not make guarantees about the order sequence of elements.
### Generic Code for overview 

```kotlin
fun main() {
    // Immutable Collections
    val immutableList = listOf(1, 2, 3)  // Immutable List
    val immutableSet = setOf("a", "b", "c")  // Immutable Set
    val immutableMap = mapOf(1 to "one", 2 to "two", 3 to "three")  // Immutable Map

    println("Immutable List:")
    for (element in immutableList) {
        println(element)
    }

    println("Immutable Set:")
    for (element in immutableSet) {
        println(element)
    }

    println("Immutable Map:")
    for ((key, value) in immutableMap) {
        println("Key: $key, Value: $value")
    }

    // Trying to modify immutable collections will result in a compilation error
    // Uncommenting the following lines will cause compilation errors

    // immutableList.add(4)
    // immutableSet.add("d")
    // immutableMap[4] = "four"

    // Mutable Collections
    val mutableList = mutableListOf(1, 2, 3)  // Mutable List
    val mutableSet = mutableSetOf("a", "b", "c")  // Mutable Set
    val mutableMap = mutableMapOf(1 to "one", 2 to "two", 3 to "three")  // Mutable Map

    println("Mutable List:")
    for (element in mutableList) {
        println(element)
    }

    println("Mutable Set:")
    for (element in mutableSet) {
        println(element)
    }

    println("Mutable Map:")
    for ((key, value) in mutableMap) {
        println("Key: $key, Value: $value")
    }

    // Modifying mutable collections is allowed
    mutableList.add(4)
    mutableSet.add("d")
    mutableMap[4] = "four"

    println("Modified Mutable List:")
    for (element in mutableList) {
        println(element)
    }

    mutableList.remove(2)  // Remove element from the mutable list
    println("Modified Mutable List after removing element:")
    for (element in mutableList) {
        println(element)
    }

    mutableSet.remove("b")  // Remove element from the mutable set
    println("Modified Mutable Set after removing element:")
    for (element in mutableSet) {
        println(element)
    }

    mutableMap.remove(3)  // Remove entry from the mutable map
    println("Modified Mutable Map after removing entry:")
    for ((key, value) in mutableMap) {
        println("Key: $key, Value: $value")
    }
}
```
[[Try it Yourself](http://jdoodle.com/ia/IGt)]

**Output**
```
Immutable List:
1
2
3
Immutable Set:
a
b
c
Immutable Map:
Key: 1, Value: one
Key: 2, Value: two
Key: 3, Value: three
Mutable List:
1
2
3
Mutable Set:
a
b
c
Mutable Map:
Key: 1, Value: one
Key: 2, Value: two
Key: 3, Value: three
Modified Mutable List:
1
2
3
4
Modified Mutable List after removing element:
1
3
4
Modified Mutable Set after removing element:
a
c
d
Modified Mutable Map after removing entry:
Key: 1, Value: one
Key: 2, Value: two
Key: 4, Value: four
```

<h3> Reference </h3>

- [Kotlin Collections](https://www.geeksforgeeks.org/kotlin-collections/)

## Functions
### Function types
- Parameters
    - Function parameters are defined using Pascal notation - name: type. Parameters are separated using commas, and each parameter must be explicitly typed.
    ```kotlin
    fun powerOf(number: Int, exponent: Int): Int { /*...*/ }
    
    // OR
     
    fun powerOf(
        number: Int,
        exponent: Int, // <- trailing comma
    ) { /*...*/ }
    ```
- Default arguments
    - Function parameters can have default values, which are used when you skip the corresponding argument. This reduces the number of overloads.
    ```kotlin
    fun foo(
        bar: Int = 0,
        baz: Int = 1,
        qux: () -> Unit,
    ) { /*...*/ }
    ```
- Named arguments
    - You can name one or more of a function's arguments when calling it. This can be helpful when a function has many arguments and it's difficult to associate a value with an argument
    ```kotlin
    fun reformat(
        str: String,
        normalizeCase: Boolean = true,
        upperCaseFirstLetter: Boolean = true,
        divideByCamelHumps: Boolean = false,
        wordSeparator: Char = ' ',
    ) { /*...*/ }
    ```
- Unit returning functions
    - If a function does not return a useful value, its return type is Unit. Unit is a type with only one value - Unit. This value does not have to be returned explicitly.
    ```kotlin
    fun printHello(name: String?): Unit {
        if (name != null)
            println("Hello $name")
        else
            println("Hi there!")
        // `return Unit` or `return` is optional
    }
    ```
- Single expressions functions
    - When a function returns a single expression, the curly braces can be omitted and the body is specified after a = symbol:
    ```kotlin
    fun double(x: Int): Int = x * 2
    ```

- Infix Notation
    - Functions marked with the infix keyword can also be called using the infix notation [omitting the dot and the parentheses for the call]. Infix function calls have lower precedence than arithmetic operators, type casts, and the rangeTo operator.  Infix functions must meet the following requirements.
        - They must be member functions or extension functions.
        - They must have a single parameter.
        - The parameter must not accept variable number of arguments and must have no default value.
        
        ```kotlin
        infix fun Int.shl(x: Int): Int { ... }
        
        // calling the function using the infix notation
        1 shl 2
        
        // is the same as
        1.shl(2)
        ```
### Lambda Functions
- Syntax of Lambda expressions
    - A lambda expression is always surrounded by curly braces, argument declarations go inside curly braces and have optional type annotations, the code_body goes after an arrow -> sign. If the inferred return type of the lambda is not Unit, then the last expression inside the lambda body is treated as return value
    ```kotlin
    // with type annotation
    val sum = {a: Int , b: Int -> a + b}
    // without type annotation
    val sum2:(Int,Int)-> Int  = { a , b -> a + b}
    ```
- Type Declarations
    - We must explicitly declare the type of our lambda expression. If lambda returns no value then we can use: Unit. 
    - Lambdas examples with return type – 
    ```kotlin
    val lambda1: (Int) -> Int = (a -> a * a)
    val lambda2: (String,String) -> String = { a , b -> a + b }
    val lambda3: (Int)-> Unit = {print(Int)}
    ```
- it: implicit name of a single parameter
    - In most cases lambdas contain the single parameter. Here, it is used to represent the single parameter we pass to lambda expression.
    ```kotlin
    ints.filter { it > 0 } // this literal is of type '(it: Int) -> Boolean'
    
    // OR return value
    
    ints.filter {
        val shouldFilter = it > 0
        shouldFilter
    }
    ```
- Function Literals with receiver
    - Function types with receiver, such as A.(B) -> C, can be instantiated with a special form of function literals – function literals with receiver.
    ```kotlin
    val lambdax: String.(Int) -> String = {this + it}
    
    val result = "Kotlin".lambdax(1)
    // in this example `this` represents `string` and `it` represents the input value
    ```
- Returning a value from lambda expression
    - After execution of lambda the final value returned by the lambda expression. Any of these Integer, String or Boolean values can be returned by the lambda function.
    ```kotlin
    val find =fun(num: Int): String{
    	if(num%2 == 0){
    		return "Even"
          }
          else{
    	      return "ODD"
          }
    }
    ```
- Anonymous Function
    - An anonymous function is very similar to a regular function except for the name of the function which is omitted from the declaration. The body of the anonymous function can be either an expression or block.
    ```kotlin
    // Function body as expression
    fun(a: Int, b: Int) : Int = a * b
    
    // Function body as block
    fun(a: Int, b: Int): Int {
        val mul = a * b
        return mul
    }
    ```
### Inline Functions
- Non local control flow
    - From the inline function, we can return from the lambda expression itself. This will also lead to exit from the function in which the inline function was called. The function literal is allowed to have non local return statements in such cases.
    
    ```kotlin
    fun main() {  
    inlineFunction({ println("calling inline functions")  
            return},{ println("next parameter in inline functions")})  
    }  
      
    inline fun inlineFunction(myFun: () -> Unit, nxtFun: () -> Unit) {  
        myFun()  
        nxtFun()  
        print("code inside inline function")  
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHn)]

    **Output**
    ```
    calling inline functions
    ```
- crossinline annotation
    - To prevent return from lambda expression and inline function itself, we can mark the lambda expression as crossinline. This will throw a compiler error if it found a return statement inside that lambda expression.
    ```kotlin
    fun main() {  
    inlineFunction({ println("calling inline functions")  
            return // compile time error  
    },{ println("next parameter in inline functions")})  
    }  
      
    inline fun inlineFunction(crossline myFun: () -> Unit, nxtFun: () -> Unit) {  
        myFun()  
        nxtFun()  
        print("code inside inline function")  
    } 
    ``` 
- noinline modifier
    - In an inline function, when we want some of the lambdas passed in the inline function to be inlined, mark other function parameters with noinline modifier. This is used to set expressions not to be inlined in the call.
    ```kotlin
    fun main() {  
    inlineFunctionExample({  println("calling inline functions")},  
                {  println("next parameter in inline functions")} )  
      
        println("this is main function closing")  
    }  
      
    inline fun inlineFunctionExample(myFun: () -> Unit, noinline nxtFun: () -> Unit  ) {  
        myFun()  
        nxtFun()  
        println("code inside inline function")  
    } 
    ``` 
### Higher Order Functions
- In Kotlin, a function which can accept a function as a parameter or can return a function is called Higher-Order function. Instead of Integer, String or Array as a parameter to function, we will pass anonymous functions or lambdas. Frequently, lambdas are passed as parameters in Kotlin functions for convenience. 

    ```kotlin

    // Pass lambda as parameter
    var lambda = {a: Int , b: Int -> a + b }
        // higher order function
    fun higherfunc( lmbd: (Int, Int) -> Int) { 
        var result = lmbd(2,4)  
        println("The sum of two numbers is: $result")
    }
    fun main() {
        higherfunc(lambda)       	//passing lambda as parameter
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHq)]

    ```kotlin
    // Pass function as parameter
    fun printMe(s:String): Unit{
        println(s)
    }
    fun higherfunc( str : String, myfunc: (String) -> Unit){
        myfunc(str)
    }
    fun main() {
        // invoke higher-order function
        higherfunc("Hello world",::printMe)
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHs)]


<h3> References </h3>

- [Functions](https://kotlinlang.org/docs/functions.html)  (Kotlin ORG)
- [Kotlin Function](https://www.javatpoint.com/kotlin-function)  (JavaTPoint)
- [Kotlin Function](https://www.geeksforgeeks.org/kotlin-functions/)  (GFG)

## OOP Concepts
### Class and objects
- **Class**
    - A class is a blueprint for creating objects (a particular data structure), providing initial values for state (member variables or fields), and implementations of behavior (member functions or methods).
    - Kotlin class is similar to Java class, a class is a blueprint for the objects which have common properties.
- **Objects**
    - Object is real time entity or may be a logical entity which has state and behavior. It has the characteristics:
        - state: it represents value of an object.
        - behavior: it represent the functionality of an object.
- Object is used to access the properties and member function of a class. Kotlin allows to create multiple object of a class.
- **Example**
    - Below example contains creating objects, access member functions and member variables.
    
    ```kotlin
    class employee {
          // Constructor Declaration of Class
        var name: String = ""
        var age: Int = 0
        var gender: Char = 'M'
        var salary: Double = 0.toDouble()
     
        fun insertValues(n: String, a: Int, g: Char, s: Double) {
            name = n
            age = a
            gender = g
            salary = s
            println("Name of the employee: $name")
            println("Age of the employee: $age")
            println("Gender: $gender")
            println("Salary of the employee: $salary")
        }
         
        fun insertName(n: String) {
            this.name = n
        }
     
    }
    fun main() {
        // creating multiple objects
        var obj = employee()
         
        // object 2 of class employee
        var obj2 = employee()
     
        //accessing the member function
        obj.insertValues("Praveen", 50, 'M', 500000.00)
     
        // accessing the member function
        obj2.insertName("Aliena")
     
        // accessing the name property of class
        println("Name of the new employee: ${obj2.name}")
     
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGN)]

    **Output** 
    ```
    Name of the employee: Praveen
    Age of the employee: 50
    Gender: M
    Salary of the employee: 500000.0
    Name of the new employee: Aliena
    ```
### Nested and Inner Class
- **Nested Classes**
    - Nested class is such class which is created inside another class. In Kotlin, nested class is by default static, so we can access the nested class property or variables using dot(.) notation without creating an object of the class.
    - Example : 
    
    ```kotlin
    class outerClass {
       private var name: String = "world new"
       class nestedClass {
           var description: String = "code inside nested class"
           private var id: Int = 101
           fun foo() {
               //  print("name is ${name}") // cannot access the outer class member
               println("Id is ${id}")
           }
       }
    }
    
    fun main() {
       // nested class must be initialize
       println(outerClass.nestedClass().description) // accessing property
       var obj = outerClass.nestedClass() // object creation
       obj.foo() // access member function
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGQ)]

    **Output** 
    ```
    code inside nested class
    Id is 101
    ```
    
- **Inner Classes**
    - When we can declare a class inside another class using the keyword inner then it is called inner class. With the help of the inner class, we can access the outer class property inside the inner class. 
    - Example:
    
    ```kotlin
    class outerClass {
       private var name: String = "Kotlin"
       inner class innerClass {
           var description: String = "code inside inner class"
           private var id: Int = 101
           fun foo() {
               println("name is ${name}") // access the outer class member even private
               println("Id is ${id}")
           }
       }
    }
    
    fun main(args: Array<String>) {
       println(outerClass().innerClass().description) // accessing property
       var obj = outerClass().innerClass() // object creation
       obj.foo() // access member function
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGS)]

    **Output** 
    ```
    code inside inner class
    name is Kotlin
    Id is 101
    ```
### Constructor
- **Primary Constructor**
    - The primary constructor is initialized in the class header, goes after the class name, using the constructor keyword. The parameters are optional in the primary constructor.
    
    ```kotlin
    fun main()
    {
        val add = Add(5, 6)
        println("The Sum of numbers 5 and 6 is: ${add.c}")
    }
    //primary constructor
    class Add constructor(a: Int,b:Int)
    {
        var c = a+b;
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IGU)]

    **Output** 
    ```
    The Sum of two numbers is: 11
    ```
    
- **Primary Constructor with initializer block**
    - The primary constructor does not contain any code. Initializer blocks are used to initialization of code. This block is prefixed with init keyword. At the period of instance initialization, the initialized blocks are executed in the same order as they appear in class body.
    
    ```kotlin
    class Person(val _name: String) {
    
        // Member Variables
        var name: String
    
        // Initializer Blocks
    
        init {
            println("This is first init block")
        }
        init {
            println("This is second init block")
        }
        init {
            println("This is third init block")
        }
        init {
            this.name = _name
            println("Name = $name")
        }
    }
    fun main() {
        val person = Person("Kotlin")
    }
    ```
    [[Try it Yourself]](http://jdoodle.com/ia/IGV)]

    **Output**
    ```
    This is first init block
    This is second init block
    This is third init block
    Name = Kotlin
    ```

- **Secondary Constructor**
    - In Kotlin, secondary constructor can be created one or more in class. The secondary constructor is created using "constructor" keyword.
        - **Class with one secondary constructor**
        
            ```kotlin
            fun main()
            {
                Add(5, 6)
            }
            //class with one secondary constructor
            class Add
            {
                constructor(a: Int, b:Int)
                {
                    var c = a + b
                    println("The sum of numbers 5 and 6 is: ${c}")
                }
            }
            ```
            [[Try it Yourself](http://jdoodle.com/ia/IGX)]

            **Output**
            ```
            The sum of numbers 5 and 6 is: 11
            ```
        
        - **Class with multiple secondary constructor**
        
            ```kotlin
            fun main()
            {
                Add(2,3)
                Add(2,3,4)
                Add(2,3,4,5)
            }
            //class with three secondary constructors
            class Add
            {
                constructor(a: Int, b: Int)
                {
                    var c = a + b
                    println("Sum of 2, 3 = ${c}")
                }
                constructor(a: Int, b: Int, c: Int)
                {
                    var d = a + b + c
                    println("Sum of 2, 3, 4 = ${d}")
                }
                constructor(a: Int, b: Int, c: Int, d: Int)
                {
                    var e = a + b + c + d
                    println("Sum of 2, 3, 4, 5 = ${e}")
                }
            }
            ```
            [[Try it Yourself](http://jdoodle.com/ia/IGZ)]

            **Output**
            ```
            Sum of 2, 3 = 5
            Sum of 2, 3, 4 = 9
            Sum of 2, 3, 4, 5 = 14
            ```
        
        - **Calling one secondary constructor from another**
        
            ```kotlin
            fun main()
            {
                Add(2,3)
            }
            class Add {
                // calling another secondary using this
                constructor(a: Int,b:Int) : this(a,b,4) {
                    var sumOfTwo = a + b
                    println("The sum of two numbers 2 and 3 is: $sumOfTwo")
                }
                // this executes first
                constructor(a: Int, b: Int,c: Int) {
                    var sumOfThree = a + b + c
                    println("The sum of three numbers 2, 3 and 4 is: $sumOfThree")
                }
            }
            ```
            [[Try it Yourself](http://jdoodle.com/ia/IH1)]

            **Output**
            ```
            The sum of three numbers 2, 3 and 4 is: 9
            The sum of two numbers 2 and 3 is: 5
            ```
### Inheritance
- Inheritance is an important feature of object oriented programming language. Inheritance allows to inherit the feature of existing class (or base or parent class) to new class (or derived class or child class).
- The main class is called super class (or parent class) and the class which inherits the superclass is called subclass (or child class). The subclass contains features of superclass as well as its own.
- In Kotlin, the derived class inherits a base class using: operator in the class header (after the derive class name or constructor).
- In Kotlin, all classes are final by default. To permit the derived class to inherit from the base class, we must use the open keyword in front of the base class.
- We can override the base member function in the derived class using the override keyword and also need to mark the member function of the base class with open keyword.
- If the derived class contains a primary constructor, then we need to initialize the base class constructor using the parameters of the derived class.
- If the derived class does not contain a primary constructor, we need to call the base class secondary constructor from the secondary constructor of derived class using the *super keyword.
    
    ```kotlin
    open class baseClass{
       val name = "Hello Kotlin"
       fun A(){
           println("Base Class")
       }
    }
    //derived class
    class derivedClass: baseClass() {
       fun B() {
           println(name)           //inherit name property
           println("Derived class")
       }
    }
    fun main(args: Array<String>) {
       val derived = derivedClass()
       derived.A()         // inheriting the  base class function
       derived.B()         // calling derived class function
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IH3)]

    **Output**
    ```
    Base Class
    Hello Kotlin
    Derived class
    ```
### Visibility Modifier
- **private**
    - The private modifier restricts the visibility of a member to the containing class only. A private member cannot be accessed from outside the class.
    
        ```kotlin
        private class A {
            private val int = 10
            fun display()
            {
                // we can access int in the same class
                println(int)  
                println("Accessing int successful")
            }
        }
        fun main(args: Array<String>){
            var a = A()
            a.display()
            // can not access 'int': it is private in class A
            println(a.int) 
        }
        ```
        [[Try it Yourself](http://jdoodle.com/ia/IH7)]

        **Output**
        ```
        Cannot access 'int': it is private in 'A'
        ```
    
- **internal** 
    - The internal modifier restricts the visibility of a member to the same *module. A module is a set of Kotlin files compiled together.
    - In below mentioned code Class A is only accessible from inside the same module. The variable int and function display() are only accessible from inside the same module, even though class B can be accessed from anywhere.
        ```kotlin
        internal class A {
        }
        public class B {
            internal val int = 10
            internal fun display() {
            }
        }
        ```
- **protected** 
    - The protected modifier restricts the visibility of a member to the containing class and its subclasses.
    
        ```kotlin
        open class A {
              // protected variable
            protected val int = 10
        }
         
        // derived class
        class B: A() {
            fun getvalue(): Int {
                  // accessed from the subclass
                return int        
            }
        }
         
        fun main(args: Array<String>) {
            var a = B()
            println("The value of integer is: "+a.getvalue())
        }
        ```
        [[Try it Yourself](http://jdoodle.com/ia/IH9)]

        **Output**
        ```
        The value of integer is: 10
        ```
    
- **public** 
    - The public modifier makes a member visible to any code. This is the default visibility for members in Kotlin.
        ```kotlin
        class A {            
            var int = 10
        }
         
        // specified with public modifier
        public class B {    
            var int2 = 20
            fun display() { 
            println("Accessible everywhere")        
            }
        }
        ```
### Abstract Class
- A class which is declared with abstract keyword is known as abstract class. An abstract class cannot be instantiated. Means, we cannot create object of abstract class. The method and properties of abstract class are non-abstract unless they are explicitly declared as abstract.

    ```kotlin
    abstract class Car {
       abstract fun run()
    }
    
    class Lambo : Car() {
        override fun run() {
            println("Lambo is running safely..")
        }
    }
    
    fun main() {
        val obj = Lambo()
        obj.run()
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHa)]

    **Output**
    ```
    Lambo is running safely..
    ```
- Bank real life example where abstraction is used
    
    ```kotlin
    abstract class Bank {  
        abstract fun simpleInterest(p: Int, r: Double, t: Int) :Double  
    }  
    class SBI : Bank() {  
        override fun simpleInterest(p: Int, r: Double, t: Int): Double{  
            return (p*r*t)/100  
        }  
    }  
    class PNB : Bank() {  
        override fun simpleInterest(p: Int, r: Double, t: Int): Double{  
            return (p*r*t)/100  
        }  
    }  
    fun main(args: Array<String>) {  
        var sbi: Bank = SBI()  
        val sbiint = sbi.simpleInterest(1000,5.0,3)  
        println("SBI interest is $sbiint")  
        var pnb: Bank = PNB()  
        val pnbint = pnb.simpleInterest(1000,4.5,3)  
        println("PNB interest is $pnbint")  
    }  
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHc)]

    **Output**
    ```
    SBI interest is 150.0
    PNB interest is 135.0
    ```


### Interface
- An interface is a blueprint of class.Kotlin interface is similar to Java 8. It contains abstract method declarations as well as implementation of method.
- Methods in an interface can have default values for its parameters. If the value for a parameter is not provided at the time of function call, then the default value is used.
- You can also inherit multiple interfaces to the class and can also inherit one interface to another.

    ```kotlin
    interface Vehicle {
       fun start()
       fun stop()
    }
    class Car : Vehicle {
       override fun start(){
           println("Car started")
       }
       override fun stop(){
           println("Car stopped")
       }
    }
    fun main(){
       val obj = Car()
       obj.start()
       obj.stop()
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHe)]

    **Output**
    ```
    Car started
    Car stopped
    ```
### Data Class
- Data class is a simple class which is used to hold data/state and contains standard functionality. A data keyword is used to declare a class as a data class.

    ```kotlin
    fun main() { 
        val u = User("Kotlin", 101, "mymail@mail.com") 
        println(u)
        println(u.name);
    } 
    data class User(var name: String, var id: Int, var email: String) 
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHg)]

    **Output**
    ```
    User(name=Kotlin, id=101, email=mymail@mail.com)
    Kotlin
    ```

### Sealed class
- Kotlin provides an important new type of class that is not present in Java. These are known as sealed classes. As the word sealed suggests, sealed classes conform to restricted or bounded class hierarchies. A sealed class defines a set of subclasses within it. It is used when it is known in advance that a type will conform to one of the subclass types. Sealed classes ensure type safety by restricting the types to be matched at compile-time rather than at runtime.

    ```kotlin
    sealed class Fruit(val x : String)
    {
        // Two subclasses of sealed class defined within
        class Apple : Fruit("Apple")
        class Mango : Fruit("Mango")
    }
     
    // A subclass defined outside the sealed class
    class Pomegranate: Fruit("Pomegranate")
     
    // A function to take in an object of type Fruit
    // And to display an appropriate message depending on the type of Fruit
    fun display(fruit: Fruit)
    {
        when(fruit)
        {
            is Fruit.Apple -> println("${fruit.x} is good for iron")
            is Fruit.Mango -> println("${fruit.x} is delicious")
            is Pomegranate -> println("${fruit.x} is good for vitamin d")
        }
    }
    fun main()
    {
        // Objects of different subclasses created
        val obj = Fruit.Apple()
        val obj1 = Fruit.Mango()
        val obj2 = Pomegranate()
     
        // Function called with different objects
        display(obj)
        display(obj1)
        display(obj2)
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHh)]

    **Output**
    ```
    Apple is good for iron
    Mango is delicious
    Pomegranate is good for vitamin d
    ```

### Extension function
- Kotlin gives the programmer the ability to add more functionality to the existing classes, without inheriting them. This is achieved through a feature known as extensions. When a function is added to an existing class it is known as Extension Function. To add an extension function to a class, define a new function appended to the classname as shown in the following example:

    ```kotlin
    class Circle(var radius : Int){
      fun area(): Int{
         return 4*radius*radius;
      }
    }
    
    fun main(){
    
      fun Circle.perimeter(): Int{
           return 2*4*radius;
       }
    
      var obj1 = Circle(2);
      println(obj1.area())
      println(obj1.perimeter());
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHi)]

    **Output**
    ```
    16
    16
    ```

<h3> Reference </h3>

- [Kotlin Classes and Objects](https://www.javatpoint.com/kotlin-class-and-object)

## Null Safety
### Nullable and Non-Nullable Types in Kotlin
- Kotlin type system has distinguish two types of references that can hold null (nullable references) and those that can not (non-null references).
- A variable of type String can not hold null. If we try to assign null to the variable, it gives compiler error.
- Below example gives compilation error
    - var s1: String = "kotlin"
    - s1 = null 
- To allow a variable to hold null, we can declare a variable as nullable string, written String? 
    - var s2: String? = "kotlin is best"
    - s2 = null // ok
### Safe Call operator(?.)
- Null Comparisons are simple but number of nested if-else expression could be burdensome. So, Kotlin has a Safe call operator, ?. that reduces this complexity and execute an action only when the specific reference holds a non-null value.. It allows us to combine a null-check and a method call in a single expression
   - name?.toUpperCase()
### Smart Cast
- In Java or other programming languages, there is a requirement of explicit type casting on the variable before accessing the properties of that variable but Kotlin does a smart casting. The Kotlin compiler automatically converts the variable to a particular class reference once it’s passed through any conditional operator.

    ```kotlin
    fun main() {
        val str1: String? = "KotlinNewWorld"
        var str2: String? = null   // prints String is null
        if(str1 is String) {
            
            // No Explicit type Casting needed.
            println("length of String ${str1.length}")
        }
        else {
            println("String is null")
        }
    }
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHj)]


### Explicit type casting
- **Unsafe cast operator : as**
    - Manually, we use the type cast operator as to cast a variable to target type. 
    - There might be possibility that we can not cast variable to target type and it throws an exception at runtime, that’s why it is called as unsafe casting.
        ```kotlin
        fun main(){
            val str1: String = "It works fine"
            val str2: String = str1 as String  	// Works
            println(str1)
        }
        ```
        ```kotlin
        fun main(){
            val str1: String? = null
            val str2: String = str1 as String  // throw exception
            println(str1)
        }
        ```
        
- **Safe cast operator : !as**
    - Kotlin also provides a facility of typecasting using safe cast operator as?. If casting is not possible it returns null instead of throwing an ClassCastException exception
    
        ```kotlin
        fun main(){
 
            var str1: Any = "Safe casting"
            val str2: String? = str1 as? String     // it works
            str1 = 11
            // type casting not possible so returns null to str3
            val str3: String? = str1 as? String   
            val str4: Int? = str1 as? Int          // it works
            println(str2)
            println(str3)
            println(str4)
        }
        ```
        [[Try it Yourself](http://jdoodle.com/ia/IHk)]

        **Output**
        ```
        Safe casting
        null
        11
        ```
    
### Elvis Operator (?:)
- Elvis operator (?:) is used to return the not null value even the conditional expression is null. It is also used to check the null safety of values.

    ```kotlin
    fun main(){  
      
        var str: String? = null  
        var str2: String? = "May be declare nullable string"  
        var len1:  Int = if (str != null) str.length else -1  
        var len2:  Int = if (str2 != null) str2.length else -1  
        println("Length of str is ${len1}")  
        println("Length of str2 is ${len2}")  
    }  
    ```
    [[Try it Yourself](http://jdoodle.com/ia/IHl)]

    **Output**
    ```
    Length of str is -1
    Length of str2 is 30
    ```
    
### NPE Operator (!!)
- not-null assertion operator (!!) converts any value to a non-null type and throws an exception if the value is null. You can write b!!, and this will return a non-null        - value of b (for example, a String in our example) or throw an NPE if b is null:
    - val a: String? = null
    - val l = a!!.length // give null pointer exception


<h3> Reference </h3>

- [Kotlin Null Safety](https://www.geeksforgeeks.org/kotlin-null-safety/) (GFG)
- [Null Safety](https://kotlinlang.org/docs/null-safety.html)(Kotlin ORG)


## Kotlin v/s Java for Android Development

| Features | Java | Kotlin |
|---|---|---|
| Primitive Type | Primitive types in Java are not objects. | Primitive types are objects. |
| Used For | It is used to develop stand-alone applications and enterprise applications. | It is used to develop server-side applications and android application development. |
| Compilation Time | Java's compilation time is pretty fast. | Its compilation time is slow in comparison to Java. |
| File Extensions | Java uses the extensions: .java (for source file), .class (for class file), .jar (for archived file). | Kotlin uses the extensions: .kt (for Kotlin source file), .kts (for Kotlin script file), .ktm (for Kotlin module). |
| Checked Exceptions | In Java, we take care of the checked exception by using the try-catch block. | There is no need to catch or declare any exception. |
| Concise | The code is not concise in comparison to Kotlin. | It reduces the boilerplate code. |
| Extension Function | We need to create a new class and inherit the parent class if we want to extend the functionality of an existing class. So, the extension function is not supported by Java. | We can extend a class with new functionality by using the extension function. |
| Widening Conversion | Java supports the implicit conversion so we can convert a smaller type to a bigger one. | Kotlin does not support the implicit conversion. So, we cannot convert the smaller type to a bigger one. |
| Code Comparison | The line of code is just doubled than Kotlin. | It reduces the line of code to half. |
| Community Support | Java provides a very large community. | Its community is not so huge as Java. |
| Casting | In Java, we need to identify and perform the casting. | Kotlin supports the smart cast, which means that it identifies the immutable type and performs implicit casting automatically. |
| Type interface | It is mandatory to specify the data type, explicitly. | It is not mandatory to specify the type of variable, explicitly. |
| Null Values | We can assign null values to variables but cannot assign null values to an object. | We cannot assign null values to any variable and objects. |
| Ternary Operator | It is available in Java. | It does not support ternary operators. |
| Coroutines Support | Multithreading feature of Java makes it more complex because managing the multiple threads is a difficult task. Java blocks the thread if we initiate a long-running intensive operation like network I/O or CPU operations. | Like Java, we can create multiple threads (long-running intensive operations) in Kotlin also but coroutine can suspend a thread execution at a certain point without blocking the other threads. |
| Functional Programming | Java is not functional programming. | It is a combination of functional and procedural programming language. |
| Data Classes | If we need a class that can hold data only, for this we need to define getter, and setter methods, constructors, and other functions. | If we want to do the same in Kotlin, we declare the class with the keyword Data. Rest the work such as creating constructor, getter, and setter methods for the fields are done by the compiler. |

## Courses
* [The Complete Kotlin Course - Mastering Kotlin from Zero](https://www.udemy.com/course/the-complete-kotlin-course-mastering-kotlin-from-zero/?utm_source=adwords&utm_medium=udemyads&utm_campaign=LongTail_la.EN_cc.INDIA&utm_content=deal4584&utm_term=_._ag_77882236463_._ad_533220806573_._kw__._de_c_._dm__._pl__._ti_dsa-1007766171312_._li_9301523_._pd__._&matchtype=&gclid=CjwKCAjwvdajBhBEEiwAeMh1U7xtvhwW7NJqyk87ebBo0MWBLJMjLgwGzC-8hAsIXaarc7FXdIyh3hoChTQQAvD_BwE) - Udemy
* [Kotlin for JAVA Developers](https://www.coursera.org/learn/kotlin-for-java-developers) - Coursera
* [Kotlin Beginner Tutorials](https://www.youtube.com/watch?v=NosAkIKgA4Y&list=PLRKyZvuMYSIMW3-rSOGCkPlO1z_IYJy3G&pp=iAQB) - YouTube

## Material:



* [https://www.javatpoint.com/kotlin-tutorial](https://www.javatpoint.com/kotlin-tutorial) - JavaTPoint
* [https://kotlinlang.org/docs/home.html](https://kotlinlang.org/docs/home.html) - Kotlin Documentation
* [https://www.geeksforgeeks.org/kotlin-programming-language](https://www.geeksforgeeks.org/kotlin-programming-language) - GeeksForGeeks


## K-words



* **super**: super keyword is used for accessing the members of the parent class like constructors, methods, variables.
* **module**: A Kotlin module is a set of Kotlin files which are considered to be interdependent and must be handled together during compilation. Kotlin packages are just like Java packages but a module is made up of one or more packages.


## References



* [https://www.codecademy.com/resources/blog/what-is-kotlin-used-for/](https://www.codecademy.com/resources/blog/what-is-kotlin-used-for/)
* [https://www.geeksforgeeks.org/introduction-to-kotlin/](https://www.geeksforgeeks.org/introduction-to-kotlin/) 
* [https://www.javatpoint.com/kotlin-tutorial](https://www.javatpoint.com/kotlin-tutorial) 
* [https://www.codexpedia.com/kotlin/install-compile-and-run-kotlin-from-command-line/](https://www.codexpedia.com/kotlin/install-compile-and-run-kotlin-from-command-line/) 
* [https://kotlinlang.org/docs/command-line.html#create-and-run-an-application](https://kotlinlang.org/docs/command-line.html#create-and-run-an-application) 
* [https://www.cyberithub.com/how-to-install-sdkman-on-linux-using-easy-steps](https://www.cyberithub.com/how-to-install-sdkman-on-linux-using-easy-steps/#:~:text=SDKMAN%20is%20a%20free%20tool,switching%2C%20removing%20and%20listing%20Candidates)
* [https://opensource.com/article/22/3/manage-java-versions-sdkman](https://opensource.com/article/22/3/manage-java-versions-sdkman#:~:text=The%20SDKMan%20project%20makes%20it,Scala%2C%20Kotlin%2C%20and%20more)
* [https://kotlinlang.org/docs/control-flow.html](https://kotlinlang.org/docs/control-flow.html) 
