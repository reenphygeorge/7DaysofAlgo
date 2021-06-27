# Code
```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("How much time does your planet take to complete a revolution around your star or Black Hole?");
        System.out.println("Days: ");
        Scanner scanner = new Scanner(System.in);
        long inputDays = scanner.nextLong();
        System.out.println("Hours: ");
        double inputHours = scanner.nextDouble();
        if (inputHours==0){
            System.out.println("Unfortunately your planet do not support the idea of a Leap year!");
        }else {
            System.out.println("How many hours do you folks have in a day?");
            double hoursInADay = scanner.nextDouble();
            scanner.close();
            daysAndLeap(inputDays, inputHours, hoursInADay);
        }
    }
    static void daysAndLeap(long days, double hours, double hoursInADay){
        int remainder= (int) ((int)hoursInADay/hours);
        System.out.println("Your planet will have "+days+" days in a year and a leap year every "+remainder+" year/s.");
    }
}


```

# Explanation
- This code outputs in how many years does a given planet will have a leap year(If exists).
- We are given the number of hours in a day and the hours left over at the end of each year.
- With these information we can estimate in how many years approximately does a leap year occur.
- Note: This code is just an approximation. For example if a given planet have 13 hours in a day and a turnover of 3 hours at the end of each year, then we can expect a leap year every 4.3 years. This code will round 4.3 to an Integer 4.
