
CODE
```
import java.util.Scanner;
public class PrimeChecker {

    public static void main(String[] args) {
        int temporary;
        boolean isPrime = true;
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter any number");
        int inputNumber = scanner.nextInt();
        scanner.close();
        if (inputNumber<=1){ //Line 1
            isPrime=false;
        }else {
            for(int i=2;i<=inputNumber/2;i++) //Line 2
            {
                temporary=inputNumber%i;
                if(temporary==0)
                {
                    isPrime=false;
                    break;
                }
            }
        }
        if (isPrime){ //Line 3
            System.out.println("True");
        }else {
            System.out.println("False");
        }
}
}

```
EXPLANATION
```
The number which is only divisible by itself and 1 is known as prime number.
A class named "PrimeChecker{}" is defined which contains the "main()" method along with all the driving code.
- Internal variable "temporary" and a boolean "isPrime" is defined for validation purpose.
- Scanner is used to retrieve the value to be evaluated and is stored in a "inputNumber".
- Line 1 checks if the input value is less than or equal to 1 in that case the number is not prime and the boolean variable is set to false.
- Line 2 checks if for "i" from 2 to inputNumber/2 [To reduce the number of computations ] the inputNumber is divisible by "i". If yes isPrime is set to false and we break out of the loop.
-Line 3 is where we check if the boolean flag is True or False and thus printing the required output.
