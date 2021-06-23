### CODE:

```java

/** Challenge 1: Spell it out 
* 
* @author Karthik._.cj
*/

import java.util.*;
public class Number
{
    static String[] letter1 = {"","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"};
    static String[] letter2 = {"Ten","Eleven","Twelve","Thirteen","Fourteen","Fifteen","Sixteen","Seventeen","Eighteen","Nineteen"};
    static String[] letter3 = {"","","Twenty ", "Thirty ", "Forty ", "Fifty ","Sixty ", "Seventy ", "Eighty ", "Ninety "};

    public static void converter1(int num)
    {
        System.out.print(letter1[num]);
    }
    
    public static void converter2(int num)
    {
        System.out.print(letter2[num]);
    }

    public static void converter3(int num)
    {
        System.out.print(letter3[num]);
    }
    public static void main(String[] args)
    {
         System.out.print("\nEnter the number of digits(1-3) : ");
         Scanner sc = new Scanner(System.in);
         int digits = sc.nextInt();
         
            if(digits > 3)
            {
                System.out.println("Be In Your Limit !!!");
            }

         else{
         int arr[] = new int[digits];
         for(int i = 0 ; i < digits ; i++)
         {
            System.out.print("\nEnter the "+(i+1)+"st digit : ");
            arr[i] = sc.nextInt(); 
         }

//---------------------------------------------------------------------------------------------------------

            if(digits == 1)
            {
                if(arr[0]==0)
                System.out.print("Zero");
                else
               {
                  for(int i = 1 ; i <= 9 ; i++)
                   {
                      if(arr[0]==i)
                       {
                         converter1(i);
                       }
                   }
               }
            }

//----------------------------------------------------------------------------------------------------------------------------

            if(digits == 2)
            {
                if(arr[0] == 1)
                {
                     for(int i = 0 ; i <= 9 ; i++)
                    {
                        if(arr[1]==i)
                        {
                         converter2(i);
                        }
                    }
                }

                for(int j = 2 ; j <= 9 ; j++)
               {
                    if(arr[0] == j)
                    {
                       converter3(j);
                         for(int i = 0 ; i <= 9 ; i++)
                       {
                            if(arr[1]==i)
                          {
                            converter1(i);
                          }
                       }
                    }
               }
            }

//---------------------------------------------------------------------------------------------------------------------

            if(digits == 3)
            {
                for(int i = 1 ; i <= 9 ; i++)
                {
                    if(arr[0]==i)
                    {
                        converter1(i);
                        System.out.print(" Hundred ");
                    }
                }

              
                if(arr[1] == 0)
                {
                    for(int i = 0 ; i <= 9 ; i++)
                    {
                        if(arr[2]==i)
                        {
                         converter1(i);
                        }
                     }
                }
               
                if(arr[1] == 1)
                {
                     for(int i = 0 ; i <= 9 ; i++)
                    {
                        if(arr[2]==i)
                        {
                         converter2(i);
                        }
                     }
                }

                    for(int j = 2 ; j <= 9 ; j++)
                    {
                        if(arr[1] == j)
                        {
                            converter3(j);
                                for(int i = 0 ; i <= 9 ; i++)
                            {
                                    if(arr[2]==i)
                                {
                                    converter1(i);
                                }
                            }
                        }
                    }
                     
                
            }
         
            sc.close();
        }
    }
       
    
}
```

### EXPLANATION:

We have 3 letters (letter1 , letter2 , letter3) of String arrays with how words are spelled.
We directly prints zero if digits is 1 and arr[0] is 0.
We print the first String array by passing the entered number as index.
If digits is 2 , converter2() is called which prints letter2.
And then inside a if condition a for loop with i=0 upto 9 converter1(i) is called and letter1 is invoked.
For every three digit , converter1() is called correspondingly .
And "Hundred" is printed.
Then converted1() , converter2() is called.
Finally in a for loop with j = 0 and j <= 9 converter3() is called and letter3 is invoked.
Then the number is converted to letters.
