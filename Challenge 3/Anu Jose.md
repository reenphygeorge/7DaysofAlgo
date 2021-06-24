#CODE
```java
import java.util.Scanner;
class Main 
{
     public static void main(String[] args)
    {
        
        System.out.println("case1 is binary to hexadecimal conversion");
        System.out.println("case2 is decimal to hexadecimal conversion");
         
        lp : while(true) 
         {
             int ch;
             Scanner sc = new Scanner(System.in);
             System.out.print("Make your choice: ");  
             ch = sc.nextInt(); 
              switch (ch)
            {
            case 1:
            
            Main ob = new Main();
            System.out.println("Enter number");
            Scanner scan= new Scanner(System.in);
            long num =scan.nextLong();
            System.out.println(ob.decimalToHex(num));
            
            break;
            case 2:
           
            System.out.println("Enter number");
            Scanner sca= new Scanner(System.in);
            int n=sca.nextInt();
            decToHexa(n);
            
            break;
           
            default:
            System.out.println("Invalid choice! Please make a valid choice. \n\n");
            }
        }
    }
 
    int binaryToDecimal(long binary)
    {
 
        int decimalNumber = 0, i = 0;
 
        while (binary > 0) 
        {
 
            decimalNumber += Math.pow(2, i++) * (binary % 10);
 
            binary /= 10;
        }
 
        return decimalNumber;
    }
 
    String decimalToHex(long binary)
    {
        
        int decimalNumber = binaryToDecimal(binary);
 
        
        String hexNumber = Integer.toHexString(decimalNumber);
 
        hexNumber = hexNumber.toUpperCase();
 
        
        return hexNumber;
    }
    
    
    static void decToHexa(int n)
    {
    
        char[] hexaDeciNum = new char[100];
 
        int i = 0;
        while (n != 0) 
        {
            
            int temp = 0;
            temp = n % 16;
 
            if (temp < 10) 
            {
                hexaDeciNum[i] = (char)(temp + 48);
                i++;
            }
            else 
            {
                hexaDeciNum[i] = (char)(temp + 55);
                i++;
            }
 
            n = n / 16;
        }
 
       
        for (int j = i - 1; j >= 0; j--)
            System.out.print(hexaDeciNum[j]);
    }
}
    
    
```

#EXPLANATION

The Hexadecimal number system has 16 entities. These 16 entities consist of 0-9  and english alphabets ranging from A through F to represent the numbers 10 to 15.
• Read the number from the user.
•Ask the user to select the choice.If the user selects choice 1 then it performs binary number to a hexadecimal number conversion and if the choice is 2 it performs decimal number to a hexadecimal number conversion by calling the function.

To convert the binary number to a hexadecimal number

•First we convert binary to decimal and then decimal to hexadecimal number.

•	To convert the binary number to a decimal number, first, extract each digit using by getting the remainder by dividing by 10.

•	Next, multiply this digit with increasing powers of 2.

•	Keep on dividing the original binary number by 10 to eliminate the last digit in each iteration.

•	After having gotten the decimal number, just use the toHexString() method to convert it to hexadecimal number.

To convert the decimal number to a hexadecimal number

•	Store the remainder when the number is divided by 16 in a temporary variable temp. If temp is less than 10, insert (48 + temp) in a character array otherwise if temp is greater than or equals to 10, insert (55 + temp) in the character array.

•	Divide the number by 16 now

•	Repeat the above two steps until the number is not equal to 0.

•	Print the array in reverse order now.



    
    
