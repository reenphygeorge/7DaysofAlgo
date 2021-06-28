# Code

```java 

import java.util.*;

public class Factors

{

	static int hcf(int a,int b)	{

		if(a==0)

			return a;

		if(b==0)

			return b;

		if(a==b)

			return a;

		if(a>b)

			return hcf(a-b,b);

		return hcf(a,b-a);

	}

	

	static int lcm(int a,int b,int high)

	{

		return (a*b)/high;

	}

	

	public static void main(String[] args)

	{

		Scanner sc= new Scanner(System.in);

		System.out.println("Enter the 2 numbers");

		int a= sc.nextInt();

		int b= sc.nextInt();

		int high= hcf(a,b);

		System.out.println("The largest number that completely divides "+a+" and "+b+" is "+high);

		System.out.println("The smallest number that is the product of both "+a+" and "+b+" is "+ lcm(a,b,high));

		sc.close(); 

	}

}

		

```

# Explanation

Euclidean algorithm is used here:

If we subtract a smaller number from the larger one, the GCD/HCF won't change.

 So if we keep subtracting repeatedly the larger of them, we'll end up with the GCD.
