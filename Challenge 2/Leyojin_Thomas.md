#code
```java
import java.util.Scanner;
public class numbers_words {
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n,m = 0,count=0,l=0,k=0,p;
		System.out.println("Enter the number in digits");
		n=sc.nextInt();
		m=n;
		if(m==0) {
			System.out.println("zero");	
		}
		while(n!=0){
	        n = n/10;
	        count++; 
		}
		if(count==1) {
			 if(m==1) { 
				System.out.println("one");	
			}else if(m==2) {
				System.out.println("two");	  
			}else if(m==3) {
				System.out.println("three");	
			}else if(m==4) { 
				System.out.println("four");	
			}else if(m==5) {
				System.out.println("five");	
			}else if(m==6) {
				System.out.println("six");	 
			}else if(m==7) {  
				System.out.println("seven");	
			}else if(m==8) {
				System.out.println("eight");	
			}else if(m==9) {
				System.out.println("nine");	
			}
		}
		if(count==2) {
			if(m==10) { 
				System.out.println("ten");	 
			}else if(m==11) { 
				System.out.println("eleven");	 
			}else if(m==12) {
				System.out.println("twelve");	
			}else if(m==13) { 
				System.out.println("thirteen");	
			}else if(m==14) {
				System.out.println("fourteen");	
			}else if(m==15) {
				System.out.println("fifteen");	
			}else if(m==16) {
				System.out.println("sixteen");	
			}else if(m==17) {
				System.out.println("seventeen");	
			}else if(m==18) {
				System.out.println("eighteen");	
			}else if(m==19) {
				System.out.println("nineteen");	
			}else {
				
					l=m%10;
					m=m/10; 
					k=m%10;   
				
				 if(k==2) {
					System.out.print("twenty");	  
				}else if(k==3) {
					System.out.print("thirty");	
				}else if(k==4) { 
					System.out.print("fourty");	
				}else if(k==5) {
					System.out.print("fifty");	 
				}else if(k==6) {
					System.out.print("sixty");	 
				}else if(k==7) {  
					System.out.print("seventy");	
				}else if(k==8) {
					System.out.print("eighty");	
				}else if(k==9) {
					System.out.print("ninety");	
				}
				 if(l==0) {
						System.out.println("");	
					}else if(l==1) {
						System.out.print(" one");	
					}else if(l==2) {
						System.out.print(" two");	  
					}else if(l==3) {
						System.out.print(" three");	 
					}else if(l==4) { 
						System.out.print(" four");	
					}else if(l==5) {
						System.out.print(" five");	
					}else if(l==6) {
						System.out.print(" six");	 
					}else if(l==7) {  
						System.out.print(" seven");	
					}else if(l==8) {
						System.out.print(" eight");	
					}else if(l==9) {
						System.out.print(" nine");	
					}
			}
		}
		if(count==3) {
			p=m/100;
			if(p==1) {
				System.out.print("one hundred ");	
			}else if(p==2) {
				System.out.print(" two hundred ");	  
			}else if(p==3) {
				System.out.print(" three hundred ");	 
			}else if(p==4) { 
				System.out.print(" four hundred ");	
			}else if(l==5) {
				System.out.print(" five hundred ");	
			}else if(p==6) {
				System.out.print(" six hundred ");	 
			}else if(p==7) {  
				System.out.print(" seven hundred ");	
			}else if(p==8) {
				System.out.print(" eight hundred ");	
			}else if(p==9) {
				System.out.print(" nine hundred ");	
			}
			m=m%100;
			if(m==10) { 
				System.out.println(" ten");	 
			}else if(m==11) { 
				System.out.println(" eleven");	 
			}else if(m==12) {
				System.out.println(" twelve");	
			}else if(m==13) {  
				System.out.println(" thirteen");	
			}else if(m==14) {
				System.out.println(" fourteen");	
			}else if(m==15) {
				System.out.println(" fifteen");	
			}else if(m==16) {
				System.out.println(" sixteen");	
			}else if(m==17) {
				System.out.println(" seventeen");	
			}else if(m==18) {
				System.out.println(" eighteen");	
			}else if(m==19) {
				System.out.println(" nineteen");	
			}
			else {
				k=m/10;
				l=m%10;
				if(k==2) {
					System.out.print(" twenty");	  
				}else if(k==3) {
					System.out.print(" thirty");	
				}else if(k==4) { 
					System.out.print(" fourty");	
				}else if(k==5) {
					System.out.print(" fifty");	 
				}else if(k==6) { 
					System.out.print(" sixty");	 
				}else if(k==7) {  
					System.out.print(" seventy");	
				}else if(k==8) {
					System.out.print(" eighty");	
				}else if(k==9) {
					System.out.print(" ninety");	
				}
				 if(l==0) {
						System.out.println("");	
					}else if(l==1) {
						System.out.print(" one");	
					}else if(l==2) {
						System.out.print(" two");	  
					}else if(l==3) {
						System.out.print(" three");	 
					}else if(l==4) { 
						System.out.print(" four");	
					}else if(l==5) {
						System.out.print(" five");	
					}else if(l==6) {
						System.out.print(" six");	 
					}else if(l==7) {  
						System.out.print(" seven");	
					}else if(l==8) {
						System.out.print(" eight");	
					}else if(l==9) {
						System.out.print(" nine");	
					}
				 }
		}
	}
	}


```
#Explanation

Save the input edigit written by the user in variable,and store the data in variable n to m.
if the value written by the user is 0 print zero ,else check for the various conditions.Check for the number of digits in that number.if the number is a single digit
go for the if condition where condition is (count==1),else if count is 2 ,go for the next if condition that is (count==2) and else go to next if condition that is (count==3)
If the digit is a single digit we can directly enter the corresponding string  and for two digit two string values required and for three digits required three strings.

