# Code
```
/*Author     : Gayathri  V
  Challenge 1: Am I prime or not?
*/

import java.util.Scanner;
public class PrimeNumChecker {

    static int check = 0;
    static void checkingMethod(int number){
        for (int count = 2; count <= number / 2; ++count) {
            if (number % count == 0) {
                check = 1;
                break;
            }
        }
        if (check != 1) {
            System.out.println(number + " is a prime number.");
        } else {
            System.out.println(number + " is not a prime number.");
        }
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Hello!!. Enter number to check Prime or Not: ");
        int number = scanner.nextInt();
        if(number != 1){
        checkingMethod(number);}
        else{ 
        System.out.println("1 is not prime or composite");
        }
    }
}


```

# Explanation
In the class "PrimeNumChecker", user able to enter a number to check Prime or not.

For the case the number is not '1', program proceed, else print it is not prime or composite.

In "checkingMethod" there is a loop and inside , a variable to count from 2 to half of entered number.
Since Prime number is not divisible by any number ,if this variable give reminder 0 for any value ,it will set the "check" as 1.
In main method considering the value of check, it will print whether number is prime or not.
Program terminates.
