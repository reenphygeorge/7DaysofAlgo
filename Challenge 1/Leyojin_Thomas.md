# Code
```java
import java.util.Scanner;
public class prime_number {
public static void main(String[] args) {
int flag=0,k;
Scanner sc=new Scanner(System.in);
System.out.println("Enter the natural number\n");
int n=sc.nextInt();
if(n==1) {
System.out.println("true");
}else {
for(int i=2;i<=n/2;i++) {
k=n%i;
if(k==0) {
System.out.println("false");
flag=1; 
break;
}	
}
if(flag==0) {
System.out.println("true");
}
}
} 
}

```

# Explanation
Prime numbers are the numbers that have only two factors, that are, 1 and the number itself.So in my code,the number entered by the user will be checked and print 'true' if it is prime and print 'false' if it is not a prime. The for loop given in the code will check whether the number entered by the user is prime or not by dividing the number starting from 2 to exactly the half of that number and the remainder is stored in variable 'k'.If the value of 'k' is 0 it will be divisible by other number' so it will not be a prime,else it will be prime.
