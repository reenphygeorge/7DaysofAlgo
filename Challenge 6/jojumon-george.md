# Code

```

 Java 

import java.util.*;

public class Planet 

{

	static int leapYear(int h,int hr)	{

		int leap=hr/h;

		return leap;

	}

	public static void main(String[] args) 

	{

		Scanner sc= new Scanner(System.in);

		System.out.print("How much time does your planet take to complete a revolution around your star or blackhole \nDays : ");

		int d= sc.nextInt();

		System.out.print("Hours : ");

		int h= sc.nextInt();

		System.out.println("How many hours do you folks have in a day? ");

		int hr= sc.nextInt();

		System.out.println("Your planet will have "+d+" days in a year and a leap year every "+leapYear(h,hr)+" years.");

		sc.close(); 

	}

}

		

```

# Explanation

The program takes the number of years to complete a revolution as the number of days in year.

Then it takes the remaining hours in the resolution time and it divides the hours in a day of the planet with it. This result is in printed as the year difference between two leap years.
