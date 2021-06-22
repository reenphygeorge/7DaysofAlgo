### CODE:

```java

/** Challenge 1: Am I prime or not? 
* 
* @author Alen Thomas Nellary
*/

import java.util.Scanner;

public class PrimeChecker {
    static boolean isPrime(int num) {
        int i;
        for(i=2; i<=num/2; i++) {
           if(num%i == 0) {
              return false;
           }
        }
        return true;
    }
    
    public static void main(String[] args) {
        int num;
        boolean prime;
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a natural number: ");
        num = scanner.nextInt();
        if(num == 1) {
           System.out.println("1 is neither Prime nor Composite!\n");
        } else {
           prime = isPrime(num);
           if(prime) {
              System.out.println("The number "+num+" is a Prime number\n");
           } else {
              System.out.println("The number "+num+" is not a Prime number\n");
           }
        }
        scanner.close();
    }
}
```

### EXPLANATION:

- In the PrimeChecker class, we have a main function and isPrime() function which returns a Boolean value, either true or false.
- In the main function we ask the user to enter a natural number.
- Then we pass this number as a parameter to the isPrime() function.
- In the isPrime() function, we run a for loop starting at value 2 till i<=num/2, incrementing it's value.
- Then return false if num%i == 0, otherwise, we return true.
- Again in the main function, we check if num == 1, it displays 1 is neither prime nor composite.
- If the returned value from isPrime() is true, we display that the number is Prime, if it is false, then display that the number is Not Prime.
