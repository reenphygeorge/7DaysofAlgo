# CODE:
```java
import java.util.*;
public class revolution {
	public static void main(String [] args) {
		Scanner s=new Scanner(System.in);
		System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
		System.out.println("Days: ");
		int d=s.nextInt();
		System.out.println("Hours: ");
		int H=s.nextInt();
		System.out.println("How many hours do you have in a day: ");
		int h=s.nextInt();
		if(H==0) {
			System.out.println("Your planet will have "+d+" days in a year and no leap years");
		}
		else {
			System.out.println("Your planet will have "+d+" days in a year and a leap year every "+h/H+" years");
		}
	}
}
```
# EXPLANATION:
- We ask the user for the days and hours it takes their planet to complete a revolution and store it as d and H.
- We also ask them how many hours they have in a day and store it as h.
- d will be the no: of days they have in a year and h/H will give us how often they have a leap year. 
