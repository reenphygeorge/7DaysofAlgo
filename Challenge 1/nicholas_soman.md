# Code
```java
import java.util.*;
public class prime {
void isprime(int n) {
	int a=0;
		for(int i=2;i<=n/2;i++) {
			if(n%i==0) {
				a=1;
				break;
			}
		}
		if(n==1) {
			System.out.println("1 is neither Prime nor Composite");
		}
		else {
		if(a==1) {
			System.out.println(n+" is not a Prime Number");
		}
		else {
			System.out.println(n+" is a Prime Number");
		}
	}
}
	public static void main(String []args) {
		Scanner s=new Scanner(System.in);
		prime p=new prime();
		System.out.println("Enter the number: ");
		int n=s.nextInt();
		p.isprime(n);
	}
}
```

# Explanation
The function isprime() checks whether the number is prime or not.
A composite number 'n' when divided through 1 to n/2 returns mod value 0 at some point(excluding 1 and n). If it does set flag=1 and break.
This is because it is divisible by a number other than 1 or n.
If the flag is 1 then it is a composite number, else prime. 
