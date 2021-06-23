#code
'''java
package Digit;

import java.util.Scanner;

public class Digit 
{
	 static void digit(int a)
	  {
	        if(a<1)
	        {
	            System.out.println("wrong input");
	        }
	        else
	        {
	            int x=a%10;//last digit
	            int y=a/10;
	            int z=y%10;//second last digit
	            int r=y/10;//first digit
	            String s []={" ","One","Two","Three","Four","Five","Six","Seven","Eight","Nine","Ten","Eleven","Twelve","Thirteen","Fourteen","Fifteen","Sixteen","Seventeen","Eighteen","Ninteen"};
	            String t []={" ","Ten","Twenty","Thirty","Fourty","Fifty","Sixty","Seventy","Eighty","Ninety"};
	            String u =" hundred ";
	            if(a<20)
	            {
	                System.out.println(s[a]);
	            }
	            else if(a<100)
	            {
	                System.out.println(t[z]+" "+s[x]);
	            }
	            else if(a>99&&a<1000)
	            {
	                System.out.println(s[r]+u+" "+t[z]+" "+ s[x]);
	            }
	       }
	  }
	         public static void main(String [] arg)
	         {
	             System.out.println("Enter the number up to three digit :");
	             Scanner sc=new Scanner(System.in);
	             int inputNumber=sc.nextInt();
	             digit(inputNumber);
	           
	        }
	    
	}
#explanation
. the input number is passed to the function digit.
. in the function first it check whether the number is greater than one or not .
. if it is smaller then it return as wrong input 
. else first we seperately taken the digits of the number.
. we have define all names in s,t arrays and the string u
. if the number is less than twenty ,it will take the number and the name from the string and print 
. like this the other condition will also check and print accordingley

