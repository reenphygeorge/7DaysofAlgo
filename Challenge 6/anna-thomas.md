Code:
```java
import java.util.Scanner;

public class YearLeap {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
		System.out.println("Days :");
		int days=sc.nextInt();
		System.out.println("Hours :");
		float hrs=sc.nextFloat();
		System.out.println("How many hours do you folks have in a day?");
		float hpd=sc.nextFloat();
		checkDays(days,hrs,hpd);
		sc.close();
	}
	public static void checkDays(int d,float h,float p) {
		float rem=h/p;
		int count=1;
		while(rem<1) {
			rem=rem*count;
			count++;}
		System.out.println("Your planet will have "+d+" days in a year and a leap year every "+count+" year/s.");
	}
}
```
Explanation:
1. Get the number of days, hours per day and extra hours from the user.
2. Calculate the decimal value between extra time and hours per day by dividing them. 
3. Find out how many times this difference occurs or how many years will it take to make it 1 day.
4. The number of years it takes to make a day is when a leap year occurs.
5. Display the number of days in a year and the occurence of a leap year.
