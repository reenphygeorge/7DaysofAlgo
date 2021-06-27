### CODE:

```java

/** Challenge 6 : Suns, blackholes and leap years 
* 
* @author karthik._.cj
*/

import java.util.*;
public class LeapYear 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("\nHow Much Time Does Your Planet Take to Complete a Revolution Around Your Star or Blackhole ? ");
        System.out.print("\nDays : ");
        int days = sc.nextInt();
        System.out.print("\nHours : ");
        int hours = sc.nextInt();
        System.out.print("\nHow Many Hours do You Folks Have In a Day : ");
        int one_day = sc.nextInt();
        int leap_year = one_day/hours;
        System.out.print("\nYour Planet Will Have "+days+" Days In a Year And a Leap Year Every "+leap_year+" Years");
        sc.close();
    }
}
```

### EXPLANATION:

- User Enters the Days and Hours that their Planets have in One Year.
- Also Enters the Hours they have in a Day.
- Then Days_hour is divided by Years_hour and the value is stored.
- Then stored value is printed.

  THANK YOU
