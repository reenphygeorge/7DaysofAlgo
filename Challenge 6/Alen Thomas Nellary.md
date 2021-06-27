### CODE:

```java

/** Challenge 6: Suns, blackholes and leap years.
* 
* @author Alen Thomas Nellary 
*/ 


import java.util.Scanner;

public class LeapYear {
	
	static void leap_year(int days, float hours, float day_hours) {
		float section = hours / day_hours;
		float leap = 1;
		while(section < 1) {
			section = section * leap;
			leap = leap + 1;
		}
		int years = (int)leap;
		System.out.println("Your planet will have "+days+" days in a year and a leap year every "+years+" years.");
	}
	
	public static void main(String[] args) {
		int days;
		float hours, day_hours;
		Scanner scanner = new Scanner(System.in);
		System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
		System.out.print("Days :  ");
		days = scanner.nextInt();
		System.out.print("Hours : ");
		hours = scanner.nextFloat();
		System.out.print("How many hours do you folks have in a day? ");
		day_hours = scanner.nextFloat();
		leap_year(days, hours, day_hours);
		scanner.close();
	}
}

```

### EXPLANATION:

- In the LeapYear class, we have a leap_year() function and a main function.
- In the main function, we accept the days, hours and also hours per day from the user and then we pass these as parameters to the leap_year() function.
- In the leap_year() function, we divide the hours by day_hours and store it in a variable section.
- While section less than 1, we multilply section with leap variable which is first initialised as 1, also incrementing the value of leap.
- Now, display the number of days in an year, along with the leap year rule of the planet.
