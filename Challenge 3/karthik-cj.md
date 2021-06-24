### CODE:

```java

/** Challenge 3: Base to Hex
* 
* @author Karthik._.cj
*/

import java.util.*;

public class Converter
{
    static String[] Hex = {"A","B","C","D","E","F"} ;

    public static void DectoHex(int n)  // Decimal(Base 10) to HexaDecimal(Base 16)
    {
        int count = 0 ;
        ArrayList<Integer> arr = new ArrayList<Integer>(); 
        while(n != 0)
        {
            arr.add(n%16);
            n = n / 16;
            count++;
        }

        Collections.reverse(arr);

        System.out.print("\nNumber in HexaDecimal : ");
        for(int i = 0 ; i < count ; i++)
        {
            if(arr.get(i) < 10)
            {
                System.out.print(arr.get(i));
            }

            if(arr.get(i) >= 10 )
            {
                int num = arr.get(i) % 10;
                System.out.print(Hex[num]); 
            }
        }
        
    }

    public static void BintoHex(Long n)  // Binary(Base 2) to HexaDecimal(Base 16)
    {
        int count = 0 , k = 0 ;
        Long val = 0L;
        ArrayList<Long> arr = new ArrayList<Long>();
        ArrayList<Long> arr1 = new ArrayList<Long>(); 
        while(n != 0)
        {
            arr.add(n%10);
            n = n / 10;
            count++ ;
        }  
            if(count % 4 == 0)
            {
                Collections.reverse(arr);
            }
            else
            {
                int addition = count % 4;
                if(addition == 1)
                {
                    for(int i = 0 ; i < 3 ; i++)
                    {
                        arr.add(0L);
                        count++;
                    }
                }

                if(addition == 2)
                {
                    for(int i = 0 ; i < 2 ; i++)
                    {
                        arr.add(0L);
                        count++;
                    }
                }

                if(addition == 3)
                {
                    for(int i = 0 ; i < 1 ; i++)
                    {
                        arr.add(0L);
                        count++;
                    }
                }

                Collections.reverse(arr);
            }
            
                for(; k < count ;)
                {
                    for(int j = 8 ; j >= 1 ; )
                    {
                        val = val + arr.get(k)*j;
                        j = j/2;
                        k++;
                    }
                    arr1.add(val);
                    val = 0L ;
                }
                
                System.out.print("\nNumber in HexaDecimal : ");
        for(int i = 0 ; i < arr1.size() ; i++)
        {
            if(arr1.get(i) < 10)
            {
                System.out.print(arr1.get(i));
            }

            if(arr1.get(i) >= 10 )
            {
                int num = (int)(arr1.get(i) % 10);
                System.out.print(Hex[num]); 
            }
        }
    }
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("\n ---------------------------------------------");
        System.out.print("\n| 1. Decimal(Base 10) to HexaDecimal(Base 16) |");
        System.out.print("\n| 2. Binary(Base 2) to HexaDecimal(Base 16)   |");
        System.out.print("\n ---------------------------------------------");
        System.out.print("\nEnter your choice (1 or 2) : ");
        int choice = sc.nextInt();

        if(choice == 1)   // Decimal(Base 10) to HexaDecimal(Base 16)
        {
            System.out.print("\nEnter the number in decimal : ");
            int num = sc.nextInt();
            DectoHex(num);
        }
        else
            if(choice == 2)   // Binary(Base 2) to HexaDecimal(Base 16)
        {
            System.out.print("\nEnter the number in Binary : ");
            long num = sc.nextLong();
            BintoHex(num);
        }
        else
            System.out.println("\nBe in your limit!!!");
            sc.close();
    }
}
```

### EXPLANATION:

User enters either (Decimal to HexaDecimal) or (Binary to HexaDecimal) value.
Then corresponding function is called.
And the value is inserted to an ArrayList digit by digit using modulus operator.
ArrayList is then reversed.
And inside a for loop , checks wheather value is above 9 and if yes corresponding String Hex[] is printed.
In Binary to Hex conversion , if count % 4 != 0 , corresponding zeros is added.
And finally inside a for loop , checks wheather value is above 9 and if yes corresponding String Hex[] is printed.
Then Base is convereted to HexaDecimal.

THANK YOU
