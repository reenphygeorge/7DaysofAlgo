#CODE

```java
import java.util.Scanner;
public class PrimeNum
{
public static boolean checkPrime(int n){
===========
for(int i=2;i<=n/2;i++)
{
        if(n%i==0){
        return false;
        }
}
return true;
===========
}
public static void main (String[] args)
{
Scanner sc= new Scanner(System.in);
System.out.println("Enter the number: ");
int n=sc.nextInt();
boolean flag=false;
System.out.println(checkPrime(n));
}
}

#EXPLANATION

•A prime number is a natural number greater than one , that is divisible only by two numbers itself and one. Two is the only even Prime number.
•	Take the input of the number to check if a number is prime . 
•	Here, Flag is initialised as false.
•	Function named ‘checkPrime’ is defined.
•	Inside the function ,For loop is used to determine if the given number ‘n’ is prime or not.
•	Here,  we are looping from 2 to n/2. It is because a number is not divisible by more than its half. we check if the number is divisible by any number in the given range
•	If ‘n’ is divisible that is  , if the remainder between the input number and the divisor is found to be zero returns false .This determines ‘n’ is not a prime number.
•	If ‘n’ isn't divisible by any number, return true and determines ‘n’ is a prime number.
