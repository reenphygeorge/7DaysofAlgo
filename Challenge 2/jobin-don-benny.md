CODE:
```

import java.util.Scanner;

public class NumberToWords {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter the number");
        int number = scanner.nextInt();
        if (number < 1 || number > 999)
            System.out.println("Please Enter a Number Between 1 and 999");
        else {
            String[] oneToNineteen = {" ", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Eleven",
            "Twelve", "Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen", "Eighteen", "Nineteen"};
            String[] tensMultiples = {" ", "Ten", "Twenty", "Thirty", "Forty", "Fifty", "Sixty", "Seventy", "Eighty", "Ninety"};


            int unit = number % 10;   // Section 1
            int twoDigits= number / 10;
            int tenth = twoDigits % 10;
            int hundred = number / 100;


            if (number < 20) {    //  Section 2
                System.out.println(oneToNineteen[number]);
            }
            else if (number < 100) {
                System.out.println(tensMultiples[tenth] + " " + oneToNineteen[unit]);
            }
            else {
                System.out.println(oneToNineteen[hundred] + " hundred " + tensMultiples[tenth] + " " + oneToNineteen[unit]);
            }
        }
    }
}
```
Explanation:

```
-This code takes any number from 1 to 999 and print its value as corresponding string.
-In Section 1 we try to separate the 'unit' , 'tens'  and 'hundreds' portion of the provided number and store them in appropriate variables.
-Section 2 is where we check the range of the numbers and map them to a predefine array of strings.

