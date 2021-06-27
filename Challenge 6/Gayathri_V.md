# Code
```java
/*
Author :Gayathri V
Challenge 6: Suns,blackholes and leap years
 */
import java.util.Scanner;
public class LeapYear {
    static void leapYear(int revolutionDays ,float dayHour , float andHours){
       float remindingHours = andHours/dayHour;
       int leapYear = 1;
       while(remindingHours < 1){
           remindingHours = remindingHours * leapYear;
           leapYear ++;
       }
        System.out.println("Your planet will have "+revolutionDays+" days in a year and a leap year every "+ leapYear +" years");
    }
    public static void main(String args[]){
        Scanner scanner = new Scanner (System.in);
        System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
        System.out.print("Days:");
        int revolutionDays = scanner.nextInt();
        System.out.print("Hours:");
        float andHours = scanner.nextInt();
        System.out.println("How many hours do you folks have in a day?");
        float dayHour = scanner.nextInt();
        leapYear(revolutionDays, dayHour , andHours);
    }
}
```

# Explanation
In the main method user able to enter the revolution day of a plant arouund the star.
And remaining hours required, also the no of houra a day belong.
In the method leapYear remaining hour is divided by the toatal hours of a day.
Obtained value is less than 1 , we can check how many years are required to combine this remaining hours and join together as a day.
The value is printed in the format till the remaing hours reached condition greater than 1.
Program terminates.
