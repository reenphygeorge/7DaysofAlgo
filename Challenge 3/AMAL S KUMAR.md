JAVA CODE
```java

import java.util.Scanner;

class Hexa
{
  int  r,n,choice; //r = remainder
  public Hexa() 
  {
    Scanner s1 = new Scanner(System.in);
    System.out.printf("Enter the choice for conversion.\n1 = decimal to hexadecimal.\n2 = binary to hexadecimal.\n");
    choice = s1.nextInt();
    if(choice == 1)
    {
      System.out.println("Enter the decimal number.");
      Scanner s2 = new Scanner(System.in);
      n = s2.nextInt();
      deciToHexa(n) ;
      
    }
    else if (choice ==2)
    {
      System.out.println("Enter the binary number.");
      Scanner s3 = new Scanner(System.in);
      String s = s3.nextLine();
      int deci =binToDeci(s);
      deciToHexa(deci);
      
    }
    else
      System.out.println("Wrong choice");
      
    
  }
  
  public void deciToHexa(int n) 
  {
    char[] hexavalues = {'0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F'};
    String H = "";
    while(n>0)
    {
      r = n%16;
      H = hexavalues[r] + H;
      n = n/16;
      
    }
    System.out.println("The corresponding hexadecimal value  = "+H);
  }
  
  public int binToDeci(String s)
  {
    int decimal = Integer.parseInt(s,2);
    return decimal;
  }
}
public class NumberConversion {

  public static void main(String[] args) 
  {
    
    Hexa h = new Hexa();

  }

}

```

Explaination:

1.Get the choice from the user.
2.If the choice is 1 then decimal to hexadecimal conversion
  Then will will pass the number to the method deciToHexa. 
  Here we use a character array to store the hexadecimal values
  (ie;from o to F)
  Then we use a while loop ,inside which we find the remainder of number(n)
  when divided by 16 and store the correspoding hexadecimal in a string H
  and reduce n by n/10.This  loop works until the value of n is greater than 0.
  After which we will print the correspoding hexadecimal value.
3.If the choice is 2 then binary to hexadecimal conversion.
  First we convert binary to decimal  using parseint() method and the transfer the decimal value to the method
  deciToHexa and then print the corresponding hexa decimal value.
 4.If the choice is any other number it will print wrong choice
