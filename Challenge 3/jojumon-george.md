# Code
```java
import java.util.*;
public class Main {
static String binToHex(int flag,long n)
{
	int []hex=new int[10];
	String[] hextable = {"0","1","2","3","4","5","6","7","8","9","A","B","C","D","E","F"};
	int l=0,temp=0;
	if(flag==2)
	{
	//grouped as hexa blocks
		int []block=new int[20];
		for(l=0;n>0;l++)
		{
			block[l]=(int)(n%10000);
			n=n/10000;
		}

		for(int i=0;i<l;i++)
		{
			temp=block[i];
			int bitt=0;
			int j=0;
			while(temp>0)
			{
				bitt=temp%10;
				temp=temp/10;
				hex[i]= hex[i]+(int)(bitt*Math.pow(2,j));
				j++;
			}
		}	
	}
	else if(flag==10)
	{
			while(n>0)
			{
				hex[l]=(int)(n%16);
				n=n/16;
				l++;
			}
	}
	else
		return ("Invalid!");
	String finalvalue="";
	for(int j=0;j<l;j++)
		finalvalue= hextable[hex[j]]+finalvalue;
	
		return finalvalue;
	}

public static void main(String[] args)
{
	Scanner sc= new Scanner(System.in);
	System.out.println("Enter base of number");
	int flag= sc.nextInt();
	System.out.println("Enter number");
	long n= sc.nextLong();
	System.out.println(binTodec(flag,n));
	sc.close();
}
}
```

# Explanation

The binToHex function is used to convert binary or decimal value to hexadecimal value. 
In case of binary value, the binaries are grouped into blocks of fore binaries each. Thereafter each block is converted into its corresponding decimal value, which in turn is converted to the hexadecimal value by referring to the hextable.
In case of decimal values, the given number is divided sequentially by 16 and the new found reminders are stored into arrays, which in turn are later converted into hexadecimal values.
