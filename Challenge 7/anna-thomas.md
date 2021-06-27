Code:
```java
import java.util.Scanner;

public class LcmHcf {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the first number");
		int fn=sc.nextInt();
		System.out.println("Enter the second number");
		int sn=sc.nextInt();
		getHcfLcm(fn,sn);
		sc.close();
	}
	public static void getHcfLcm(int x,int y) {
		int f=x;
		int s=y;
		while(y!=0) {
			int temp=y;
			y=x%y;
			x=temp;
		}
		int hcf=x;
		int lcm=(f*s)/hcf;
		System.out.println("The largest number that completely divides "+f+" and "+s+" is "+hcf+" and the smallest number that is the product of "+f+" and "+s+" is "+lcm);
	}
}
```
Explanation:
1. Get the numbers from the user(fn and sn).
2. To get HCF we need to find out the remainder we get while dividing both fn and sn.
3. When the remainder is 0, we exit the loop and store the value of sn that gave the remainder 0.(that is the hcf)
4. To get LCM we can use the formula fn * sn=LCM * HCF.
