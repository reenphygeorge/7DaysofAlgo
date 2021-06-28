# CODE:
```java
import java.util.*;
public class factorsandmultiples {
	public static void main(String [] args) {
		Scanner s=new Scanner(System.in);
		int a=0,b=0,c=0;
		System.out.println("Enter two numbers: ");
		int n1=s.nextInt();
		int n2=s.nextInt();
		for(int i=1;i<=n1||i<=n2;i++) {
			if(n1%i==0&&n2%i==0) {
				a=i;
			}
		}
		System.out.println("GCD: "+a);
		b=(n1*n2)/a;
		System.out.println("LCM: "+b);
	}
}

```
# EXPLANATION:
- To find GCD we use a for loop. We use an if condition (n1%i==0&&n2%i==0) inside the for loop to check which is the smallest no: that divides both the numbers.
- LCM= (n1*n2)/gcd.
