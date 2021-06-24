Code 
```java
import java.util.Scanner;

public class ToHexa {

	public static void main(String[] args) {
		System.out.println("Enter the number:");
		Scanner sc=new Scanner(System.in);
		int num=sc.nextInt();
		int count=0;
		String temp=Integer.toString(num);
		for(int i=1;i<=temp.length();i++) {
			if(temp.charAt(i-1)=='0' || temp.charAt(i-1)=='1') {
				count++;
			}
		}
		if(count==temp.length()) {
			fromBin(num,temp.length());
		}else {
			fromDec(num,temp.length());
		}
		sc.close();
	}
static void fromBin(int x,int n) {
	int ld=0,pow=1,newnum=0,s=n;
	while(n!=0){
			ld=x%10;
			newnum=newnum+(ld*pow);
			pow=pow*2;
			n--;
			x=x/10;
		}
	fromDec(newnum,s);
}
static void fromDec(int x,int n) {
	int[] arr=new int[n];
	String[] arr2=new String[n];
	for(int i=0;i<n;i++) {
		if(x!=0) {
		arr[i]=x%16;
		x=x/16;
		arr2[i]=Integer.toString(arr[i]);
		}
	}
	for(int i=n-1;i>=0 ;i--) {
		if(arr2[i]!=null) {
		if (arr[i]>9) {
			printNum(arr[i]);
		}else {
			System.out.print(arr[i]);
		}}
	}
}
static void printNum(int x) {
	switch(x) {
	case 10:
		System.out.print("A");
		break;
	case 11:
		System.out.print("B");
		break;
	case 12:
		System.out.print("C");
		break;
	case 13:
		System.out.print("D");
		break;
	case 14:
		System.out.print("E");
		break;
	case 15:
		System.out.print("F");
		break;
	default:
		break;
	}
}
}
```
Explanation:
1. Get the number from the user.
2. Identify whether its binary or decimal (by counting the number of 1's and 0's and comparing with the total length).
3. If it is a decimal number, using an integer array store the remainders (obtained while dividing by 16) and reduce the quotient in each go by dividing it by 16 until quotient becomes 0.
4. By converting the integer array to string array the null values are removed.
5. If the value is greater than 9, then it directs to method printNum (where the alphabets assigned to the number is printed) else the number is printed.
6. If it is a binary number, it is first converted to decimal.
7. To obtain decimal from binary, the last digit is extracted and multiplied by 2 every time and these are added(newnum) until the number(x) becomes 0 (number is divided by 10 every time until then).
8. Then the same method used in decimal is followed.
