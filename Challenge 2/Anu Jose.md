#CODE
```java
import java.util.Scanner;
public class NumToWord
{
    public static void main(String args[])
    {
        String[] singles = {"","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"};
        String[] tens = {"","","Twenty","Thirty","Fourty","Fifty","Sixty","Seventy","Eighty","Ninety"};
        String[] tenPlus = {"","Eleven","Twelve","Thirteen","Fourteen","Fifteen","Sixteen","Seventeen","Eighteen","Nineteen"};
        System.out.println("Enter the number");
        Scanner in = new Scanner(System.in);
        String numString = in.nextLine();
        int num = Integer.parseInt(numString);
        int tempNum = num,i=0;
        String resultString="";
		if(numString.length()<=3)
		{
            while(tempNum>0)
            {
              i++;
              int rem = tempNum%10;
			  if(((tempNum%100)>10) && ((tempNum%100)<20) && i==1)
			  {
				resultString = tenPlus[(tempNum%100)-10]+resultString;
				i++;
				tempNum = tempNum/10;
			  }
			  else
			  {
				if(i==1)
				{
                resultString = singles[rem]+" "+resultString;
				}
				if(i==2)
				{
                resultString = tens[rem]+" "+resultString;
				}
		      }
         if(i==3)
          {
				 if(rem!=0)
				  {
					resultString = singles[rem]+" Hundred "+resultString;
				  }
               }
               
               tempNum = tempNum/10;
        }
		}else{
			System.out.println("limit exceeded");
		}
        System.out.println(resultString);
    }
    
}
```

#EXPLANATION

1.Read the number from the user.

2.create arrays that store individual parts of output strings.

3.One array is used for storing  single digits, one for numbers from 11 to 19, one for 20, 30,50,60,70,80,90.

4.we employee a recursive formula extracting numbers from right to left , inorder to transform our input number into its corresponding word.
  For example,If the number is 123, 123 mod 10 taken then the remainder is 3 which is the  last digit then we divide 123 by 10 ,then number will become 12. 
  The same process repeated that 12 mod 10 taken then the remainder is 2 and 12/10 will give 1.Simalarly each number can be extracted from right to left.
  
5.The words extracted ech time is concantenated to the resultstring
  
