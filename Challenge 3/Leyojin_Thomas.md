### code
```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class to_hexadecimal {
public static void main(String [] args) {
	Scanner sc =new Scanner(System.in); 
	Long k=0L,x;
	int y=0,f;
	long a = 0;
	Long count=0L;
	System.out.println("which type of number wanted to convert to hexadecimal");
	System.out.println("press 1 for binary, press 2 for decimal");
	Long m=sc.nextLong();
	System.out.println("enter the number to convert");
	Long n=sc.nextLong();
	if(m==2) {
		ArrayList<Long> num=new ArrayList<Long>();
		if(n<16) {
			if(n<10) { 
				System.out.println(n); 
			}else { 
				if(n==10) {
					System.out.println("A");
				}if(n==11) {
					System.out.println("B");  
				}if(n==12) {
					System.out.println("C");
				}if(n==13) {
					System.out.println("D");
				}if(n==14) {
					System.out.println("E"); 
				} if(n==15) {
					System.out.println("F");
				}
			}
		}else{ 
			while(n!=0) { 
				 k=n%16;
				 count++;
				 num.add(k);  
				 n=n/16; 
			}  
			Collections.reverse(num); 
			for(int i=0;i<count;i++) {
			if(num.get(i)>9) {
				Long z=num.get(i); 
				if(z==10) {
					System.out.print("A");
				}if(z==11) {
					System.out.print("B"); 
				}if(z==12) {
					System.out.print("C");
				}if(z==13) {
					System.out.print("D");
				}if(z==14) {
					System.out.print("E");  
				} if(z==15) {
					System.out.print("F");
				}
			}else {
				System.out.print(num.get(i));
			}
			}
		
		
		
		}
	}else if(m==1) {
		ArrayList<Long> dec=new ArrayList<Long>();
		while(n!=0) { 
			 k=n%10;
			 count++;
			 dec.add(k);  
			 n=n/10; 
		}//Collections.reverse(dec);
		for( ;y<count;) {
			for( f=1;f<=8;) {
			a=a+dec.get(y)*f;
			f = f*2; 
			y++;} 
			
			ArrayList<Long> num1=new ArrayList<Long>();
			if(a<16) {
				if(a<11) { 
					System.out.println(n);
				}else {
					if(a==10) {
						System.out.println("A");
					}if(a==11) {
						System.out.println("B"); 
					}if(a==12) {
						System.out.println("C");
					}if(a==13) {
						System.out.println("D");
					}if(a==14) { 
						System.out.println("E"); 
					} if(a==15) {
						System.out.println("F");
					}
				} 
			}else{  
				while(a!=0) { 
					 k=a%16;
					 count++;
					 num1.add(k);  
					 a=a/16;  
				}  
				Collections.reverse(num1); 
				for(int i=0;i<num1.size();i++) {
				if(num1.get(i)>9) {
					Long z=num1.get(i); 
					if(z==10) {
						System.out.print("A");
					}if(z==11) {
						System.out.print("B"); 
					}if(z==12) {
						System.out.print("C"); 
					}if(z==13) {
						System.out.print("D");
					}if(z==14) {
						System.out.print("E");  
					} if(z==15) {
						System.out.print("F");
					}
				}else {
					System.out.print(num1.get(i));
				}
				}
			}	
	}
}
}
		 }
```
### Explanation
In this program we can convert a binary and decimal numbers can be converted into hexadecimal.
If the user wanter to convert a binary then moves to first condition else moves to second.
to covert decimal  into  hexadecimal first divide the decimal  with 16 and stores the remainder and print them.
If the remainder is greater that 9  then display the corresponding alphabet.
In case of binary to hexadecimal convert the binary to decimal then to hexadecimal .
