JAVA CODE

```java

import java.util.Scanner;
class Prime
{
  int n,i;
  boolean flag = true;
  public int input() {
  Scanner sc = new Scanner(System.in);
  System.out.println("Enter the natural number to check wheather prime or not.");
  n = sc.nextInt();
  return n;
  }
  public boolean isPrime(int n) {
    if (n == 1)
    {
      System.out.println(n+" is neither prime nor composite");
      return false;
    }
    else {
      for(i = 2;i<=n/2;i++)
      {
        if(n%i == 0)
          flag = false;
          break;
      }
      return flag;
    }
    
  }
  
  
}
public class PrimeCheck {

  public static void main(String[] args) {
    int numb;
    Prime p = new Prime();
    numb= p.input();
    System.out.println(p.isPrime(numb));

  }

}

```

EXPLANATION

A prime number is a number which is divisble by only two numbers:1 and the number itself.

*.In the main class(PrimeCheck)we are creating the object(p) of class Prime.
  So that we can call the functions of class Prime using its object p.
  
*.Now we will ask the user to enter the number to check whether the number 
  is prime or not by calling the input() function of class Prime using p.
  It will return the integer value entered by the user to the variable numb.
  
*.Then we will check  whether the number is prime or not by calling the 
  function isPrime(),we pass the number stored in numb to isPrime()
  function.  And we also initialsed the value of flag variable as true.
  
*.In the isPrime() function first we check whether the number(n) entered 
  is 1 or not.If 1 it will print "n is neither prime nor composite" and 
  return "false" Since it is  neither prime nor composite.
  
*.Else we run a for loop,we will check if the number(n) is divisible by  
  any number in the given range(2 to n/2)
  
    #)if n is divisible ,flag is set to "false" and we break out of the 
      loop.This indicates that n is not prime since it is divisible by 
     other numbers rather than 1 and n itself.
    #)If not divisible after the range(ie;>n/2)it comes out of loop and 
      flag reamains "true",indicates number is prime.
    #)Then it will print the value of flag(ie;true or false)
