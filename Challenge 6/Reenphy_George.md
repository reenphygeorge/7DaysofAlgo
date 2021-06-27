# Code
```
import java.util.*;

class Main {
    
    public static float leap(Float rev_hrs, Float hrs) {
        return(1/(rev_hrs/hrs));
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("How much time does your planet take to complete a revolution around your star or blackhole?");
        System.out.println("Days: ");
        int rev_days=sc.nextInt();
        System.out.println("Hours: ");
        float rev_hrs=sc.nextFloat();
        System.out.println("How many hours do you folks have in a day?");
        float hrs=sc.nextFloat();
        int lp_yr=(int)leap(rev_hrs,hrs);
        System.out.println("Your planet will have "+rev_days+" days in a year and a leap year every "+lp_yr+" years.");
    }
}

```

# Explanation
```
1. User is asked to enter all the required data.

2. Now the leap() method is called, which takes no of extra hours taken for one revolution and no of hours in one day as the argument.

3. Inside the method, the extra hours taken will be converted to days by dividing it with no of hours in one day.

4. A particular year will become a leap year only when the above calculated value becomes '1'.
We can find that by just dividing '1' by it.

5. The method returns the planet's leap year rule. It would be a float value, which will be typcasted to int while printing.

6. The no of days entered will also be printed along with the leap year rule.

```