#code
'''Java
package Hexa;
import java.util.*;
public class Hexa {
     
	  static void decimalHexa(int num)
	  {
		  int reminder;
		  char[] hexa= {'0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F',};
		  String hexaValue="";
		  while(num>0)
		  {
			  reminder=num%16;
			  hexaValue=hexa[reminder]+hexaValue;
			  num=num/16;
		  }
		  System.out.println("Hexa value is:"+hexaValue);
		  
	  }
	public static void main(String[] args) {
		System.out.println("Enter the base");
		Scanner sc=new Scanner(System.in);
		int base=sc.nextInt();
		if(base==2)
		{
		System.out.println("Enter the number in binary");
		Scanner s=new Scanner(System.in);
		String inputNumbe=s.nextLine();
		//binaryDec(inputNumbe);
		int decimal = Integer.parseInt(inputNumbe, 2);
		decimalHexa(decimal);
		}
		if(base==10)
		{
		System.out.println("Enter the number in decimal");
		Scanner s1=new Scanner(System.in);
		int inputNumber=s1.nextInt();
	     decimalHexa(inputNumber);
		}
	     

	}

}
#explanation
. in the main function it ask the user for base
. if the base is 2 then its binary number will bought from the user
. then it is converted to the decimal 
. then it is passed as a parameter to the function decimalHexa
. if the base is 10 then it directly call the function decimalHexa
. at the function decimaHexa it find the remainder and store it to an array
. the we reverse print it
