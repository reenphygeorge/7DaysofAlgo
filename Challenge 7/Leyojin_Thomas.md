### code
```java
import java.util.Scanner;
public class lcm_hcf {
public static void main(String [] args) {
	Scanner sc=new Scanner (System.in);
	int min=0;
	int hcf = 0,lcm = 0;
	System.out.println("enter the first number");
	int a=sc.nextInt();
	System.out.println("enter the second number");
	int b=sc.nextInt();
	if(a<b) {
	 min=a; 
	}else 
	min=b;
	for(int i=1;i<=min;i++) {
	if(a%i==0 && b%i==0) {
	hcf=i;	 
	}
	}
	lcm=(a*b)/hcf;
	System.out.println("hcf= "+hcf+"  lcm= "+lcm);
}
}
```
### Explanation
In this program we are finding hcf and lcm by java code, 
lcm is the least common multiple and hcf is the highest commom factor.
If any digit less than the given two numbers can be divide both the numbers with remainder 0 the it is considered as hcf ,
iterating this code upto  one of the digit entered by the user ,the largest of hcf is selected. 
Lcm when multiplied by hcf will give the product of the 2 numbers with this logic  we can also find lcm with hcf.
