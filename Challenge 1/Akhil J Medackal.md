# Code
'''java
package Primenumber;
import java.util.Scanner;
public class Primenumber {
	int inputNumber;
 static boolean checkPrime(int inputNumber)
	{
		int i;
		boolean isPrime=true;
		if(inputNumber<=1)
		{
			isPrime=false;
			return isPrime;
		}
		 else {
			for(i=2;i<inputNumber/2;i++)
			{
				if(inputNumber%i==0)
				{
					isPrime=false;
					break;
				}
			}
      return isPrime;
	}
}
 public static void main(String[] args)
 {
	System.out.println("Enter the number :");
	Scanner sc=new Scanner(System.in);
	int inputNumber=sc.nextInt();
	 boolean isPrime=checkPrime(inputNumber);
	 if(isPrime==false)
	 {
		 System.out.println(inputNumber +" "+"is not a prime number");
	 }
	 else {
		 System.out.println(inputNumber +" "+"is a prime number");
	 }
 }
}
,,,

# Explanation
A number is said to be prime number when it satisfies two condition
1. The number should be greater than one
2. The number should be divisible only by one and itself
In the class Primenumber we have a method checkPrime which returns the value true or false.
We ask the user to enter the number to be checked in the main fuction.
Then we call the checkPrime function.
This number is passed as parameter to our method.
First we set isPrime value as true.
In the method first it check whether the number is <=1
If the condition is true it returns the value of isPrime as False
else we run a for loop starting from i=2 to i<inputNumber/2
It returns false if (inputNumber%i==0) otherwise it returns isPrime value as true.
If the returened value of isPrime true then we print it as a prime number otherwise as not a prime number.
