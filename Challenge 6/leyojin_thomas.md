### code
``` java
import java.util.Scanner;

public class year {
public static void main(String[] args) {
	Scanner sc=new Scanner(System.in);
	int year,days,hour,per_day;
	System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
	//year=sc.nextInt();
	System.out.println("Days :");
	days=sc.nextInt();
	System.out.println("Hours :");
	hour=sc.nextInt();
	System.out.println("How many hours do you folks have in a day?");
	per_day=sc.nextInt();
	 year_calculator(days,hour,per_day);
}

public static void year_calculator(int days,int hour,int per_day) {
	 int leap=per_day/hour;
	 System.out.println("Your planet will have "+days+"days in a year and a leap year every "+leap+" years");
}


}
