CODE:
```java
import java.util.*;
public class BorDtoHexadecimal {
    public static void main(String[] args) {
        System.out.println("Enter 1 for binary to Hex and 2 for Decimal to Hex");
        Scanner scanner = new Scanner(System.in);
        int choice = scanner.nextInt();
        System.out.println("Enter the Number to be converted");
        int number = scanner.nextInt();
        if(choice==1){
            binaryToDecimal(number);
        }else{
            decimalToHexadecimal(number);
        }

    }
     static  void binaryToDecimal(int value){
         String binary=String.valueOf(value);
         int decimal = Integer.parseInt(binary, 2);
         decimalToHexadecimal(decimal);

     }
     static void decimalToHexadecimal(int value){
         int remainder;
         StringBuilder string= new StringBuilder();
         char[] hex ={'0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F'};
         while(value>0)
         {
             remainder=value%16;
             string.insert(0, hex[remainder]);
             value=value/16;
         }
         System.out.println("Hexadecimal Value is : "+string);
     }

     }

```
Explanation:
```java
- This code converts either Binary to Hexadecimal or Decimal to Hexadecimal based on the choice you make.
- First we obtain the number to be converted from the user.
- Based on the choice made by the user the number is either transferred to binaryToDecimal() or to the decimalToHexadecimal() method.
- The binaryToDecimal() method is to convert the binary inputs first to decimal so that it can be trnsferred to the decimalToHexadecimal() method.
