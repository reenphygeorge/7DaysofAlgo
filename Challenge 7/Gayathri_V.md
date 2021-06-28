# Code
```java
/*
Author : Gayathri V
Challenge 6: Factors and Multiples.
 */
import java.util.Scanner;
public class HCFAndLCM
{
    static void lcmAndHcf(int number1 , int number2){
       int copy1 = number1;
       int copy2 =number2;
       int storage , hcf ,lcm;
        while(copy2 != 0)
        {
            storage = copy2;
            copy2 = copy1%copy2;
            copy1 = storage;
        }
        hcf = copy1;
        lcm = (number1*number2)/hcf;
        System.out.print("HCF = " +hcf);
        System.out.print("\nLCM = " +lcm);
    }
    public static void main(String args[])
    {
        int number1, number2;
        Scanner scan = new Scanner(System.in);
        System.out.print("Enter Two Number : ");
        number1 = scan.nextInt();
        number2 = scan.nextInt();
        lcmAndHcf(number1,number2);
    }
}
```

# Explanation

User can enter two numbers using main method.
The numbers are goes into the static method and a copy of numbers are made.
Dividing the numbers while they are not equal to zero and reminder get stored
And replaced as new number for division with help of temporary location.
Hcf will be the final reminder and lcm obtained by number1 multiplied by number2 and divided by obtained hcf.
Printed the HCF and LCM and program terminates.
