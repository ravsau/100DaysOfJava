
## Part 1: 

Start from this file. 

```java
import java.security.SecureRandom;

public final class Day001 {

    public static final SecureRandom SECURE_RANDOM = new SecureRandom();

    public static void main(String[] args) {
        System.out.println("Generating a number between 50 and 100...");
        System.out.println(randomNumberBetween(50, 100));
    }

    private static int randomNumberBetween(int minimum, int maximum) {
        return SECURE_RANDOM.nextInt(maximum - minimum) + minimum;
    }

}
```



Steps: 
- Save as Day001.java and Compile program 
```bash
javac Day001.java
```

- Run the program 

```
java Day001.java 
```

Output will be something like 

```
Generating a number between 50 and 100...
73
```
----
## Part 2

Add input from users to get the two numbers. 

```java

import java.security.SecureRandom;
import java.util.Scanner;  // Import the Scanner class required for user input

public final class Day001 {

    public static final SecureRandom SECURE_RANDOM = new SecureRandom();

    public static void main(String[] args) {
        Scanner myObj = new Scanner(System.in);
              

          System.out.println("Enter a number");

          int number1 = myObj.nextInt();  // Read user integer input

      
          System.out.println("Enter another number");

          int number2 = myObj.nextInt();  
   
        System.out.println("Generating a number between "+ number1+" and "+number2);
        System.out.println(randomNumberBetween(number1, number2));
    }

    private static int randomNumberBetween(int minimum, int maximum) {
        return SECURE_RANDOM.nextInt(maximum - minimum) + minimum;
    }



}


```



Run the program 

```
$ javac Day001.java 
$ java Day001
Enter a number
10
Enter another number
20
Generating a number between 10 and 20
14


$ java Day001
Enter a number
2   
Enter another number
3
Generating a number between 2 and 3
2
```

Checkpoint: 
- we have successfully added user input 



