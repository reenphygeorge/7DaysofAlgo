# Code
```
import java.util.*;

class Main
{
	public static boolean isPrime(int n) {
	    for(int i=2;i<n/2;i++) {
	        if(n%i==0) {
	            return false;
	        }
	    }
	    return true;
	}
	public static void main (String[] args) throws java.lang.Exception
	{
		Scanner sc = new Scanner(System.in);
		int n=sc.nextInt();
		boolean result = isPrime(n);		
		System.out.println(result);
	}
}
```

# Explanation
- Prime numbers are the positive integers having only two factors, 1 and the integer itself.

- Imagine **n** is the number to be checked.

- So to check whether **n** is prime, we've to check for any factors of **n** from 2 to n-1.

- In this case the time complexity is **O(n)**.

- Actually we don't have to check upto n-1. We just have to check upto the floor value of n/2.

- Consider n = 15, floor value of n/2 becomes 7. So we will check from 2 to 7. 

- Imagine we are checking till 8. But 8 * 2 = 16. So there is no chance for 8 to be a factor of 15. This is the same case with all numbers greater than 7.

- Now the time complexity is decreased to **O(n/2)**.

- Thus by this method we can check whether a number is prime or not, more efficiently.
