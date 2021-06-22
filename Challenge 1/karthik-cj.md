# Code


import java.util.Scanner;
public class Prime
{
    static boolean PrimeCheck(int num) 
    {
        for(int i = 2; i <= num/2; i++) 
        {
           if(num%i == 0) 
           {
              return false;
           }
        }
        return true;
    }
    
    public static void main(String[] args) 
    {
        boolean prime;
        int num;
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a natural number(1 - ∞) : ");
        num = sc.nextInt();
        if(num == 1) 
        {
           System.out.println("\n1 is neither Prime nor Composite");
        } 
        
           else 
        {
           prime = PrimeCheck(num);
           
           if(prime) 
           {
              System.out.println("\nThe number "+num+" is a Prime number");
           }
           
           else 
           {
              System.out.println("\nThe number "+num+" is not a Prime number");
           }
        }
            sc.close();
    }
}


# Explanation

- We have a PrimeCheck() function which returns either true or false.
- We pass a number to PrimeCheck() function.
- In the PrimeCheck() function , loop starting from 2 till i <= num/2 and increments value.
- Returns false if num%i == 0 , else return true.
- Again checks if num == 1 , and displays 1 is not composite nor prime.
- If value returned from PrimeCheck() is true , displays the number is Prime , else displays the number is Not Prime.
