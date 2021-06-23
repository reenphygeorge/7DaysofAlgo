JAVA CODE

```java

import java.util.Scanner;

class SpellItOut
{
	int  n,r,s,f,temp;
	//String  s1,s2,s3;
	
	public int input() {
		
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the number (range 0-999).");
		n = sc.nextInt();
		return n;
		
	}
	public  void logic(int n) {
	r = n % 10;      //last digit
	temp = n / 10;
	s = temp % 10;   //2nd digit
	f = n/100;       //1st digit
	String s1[] = {" ","One","Two","Three","Four","Five","Six","Seven","Eight","Nine","Ten","Eleven","Twelve","Thirteen","Fourteen","Fifteen","Sixteen","Seventeen","Eighteen","Ninteen"};
	String s2[] = {" ","Ten","Twenty","Thirty","Forty","Fifty","Sixty","Seventy","Eighty","Nintey"};
	String s3 = "Hundred";
	 
	if (n==0)
		System.out.println("zero");
	else if (n<20 && n!=0)
		System.out.println(s1[n]);
	else if(n<100)
		System.out.println(s2[s]+" "+s1[r]);
	else
		System.out.println(s1[f]+" "+s3+" "+s2[s]+" "+s1[r]);
		
	}
	
}
public class Spellit {

	public static void main(String[] args) {
		int numb;
		SpellItOut s = new SpellItOut();
		numb = s.input();
		s.logic(numb);

	}

}


```

Explaination:

1.Get the number from the user,ranges from 0 to 999.
2.Pass the number to the function logic.
3.Find the first ,second and the last digit of number.
4.Create three strings s1,s2,s3.
  First string has spelling of numbers less than 20(ie; one to ninteen).
  Second string has spelling of numbers which is multiple of 10(from ten to ninty).
  Third string stores the value hundred.
5.If number is zero it will print zero.
6.If number is less than 20,then it will print (s1[number]).
7.If number  is less than 100,then it will print( s2[first digit] + s1[second digit]) .
8.If number  is 100 or greater than 100,then it will print( s1[first digit]+s3+s2[second digit] + s1[first digit])
