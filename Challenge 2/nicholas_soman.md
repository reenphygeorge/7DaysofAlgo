#CODE
```java
import java.util.*;
class three{
	String [] d= {"OneHundred ","TwoHundred ","ThreeHundred ","FourHundred ","FiveHundred ","SixHundred ","SevenHundred ","EightHundred ","NineHundred "};
	void threedigit(int n) {
	System.out.print(d[n-1]);
	}
}
class two{
	void twodigit(int n) {
		String [] a= {"Zero","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"};
		String [] b={"Ten","Twenty","Thirty","Fourty","Fifty","Sixty","Seventy","Eighty","Ninety"};
		String [] c= {"Eleven","Twelve","Thirteen","Fourteen","Fifteen","Sixteen","Seventeen","Eighteen","Nineteen"};
		
		int l1=n/10;
		int l2=n%10;
		if(l2==0) {
			System.out.println(b[l1-1]);
		}
		else if(l1==1) {
			System.out.println(c[l2-1]);
		}
		else {
			System.out.println(b[l1-1]+" "+a[l2]);
		}
	}
}
public class numberchanger {
	void spellit(int n) {
		int p= String.valueOf(n).length();
		String [] a= {"Zero","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"};
		two t=new two();
		three th=new three();
		if(p==1) {
			System.out.println(a[n]);
		}
		if(p==2) {
			t.twodigit(n);
		}
		if(p==3) {
			int k1=n/100;
			int k2=n%100;
			int k3=k2/10;
			int k4=k2%10;
			if(k4==0&&k3==0) {
			   th.threedigit(k1);
			}
			else if(k3==0&&k4!=0) {
				th.threedigit(k1);
				System.out.println(a[k4]);
			}
			else {
				th.threedigit(k1);
				t.twodigit(k2);
			}
		}
	}
	public static void main(String [] args) {
		Scanner s=new Scanner(System.in);
		numberchanger nc=new numberchanger();
		System.out.println("Enter the number: ");
		int n=s.nextInt();
		nc.spellit(n);
		s.close();
	}
}
#EXPLANATION
We have 4 sets of String arrays based on how different words are spelled.
One-Digit:
We print the first String array by passing the entered number as index.
Two-Digit:
We split the number into 2 and store it in two int variables(l1-tens place,l2-ones place) using % and /.We treat l2 the same way as a one-digit number.We print the second String array by passing l1 as index.
Three-Digit:
We split the number into 4 and store it in four int variables(k1-hundreds place,k2-two digit no:,k3-tens place,k4-ones).We traet k2 the same way as two-digit no:.So we pass k2 into twodigit().We print the second String array by passing l1 as index.
