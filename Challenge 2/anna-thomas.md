Code:
```c
import java.util.Scanner;

public class Spelling{
public static void main(String[] args) {
	System.out.println("Enter the number: ");
	Scanner sc=new Scanner(System.in);
	int n=sc.nextInt();
	spellNum(n);
	sc.close();
}
static void spellNum(int x) {
	String temp=Integer.toString(x);
	int count=temp.length();
	if(x==0) {
		System.out.print("Zero");
	}
	for(int i=1;i<=temp.length();i++) {
		if(temp.charAt(i-1)!='0') {
		switch(count) {
		case 4:
			printnum(temp.charAt(i-1));
			System.out.print(" Thousand ");
			break;
		case 3:
			printnum(temp.charAt(i-1));
			System.out.print(" Hundred ");
			break;
		case 2:
			if (temp.charAt(i-1)=='1') {
				printones(temp.charAt(i));
				count--;
			}else if (temp.charAt(i-1)!='1') {
				printtens(temp.charAt(i-1));
			}
			break;
		case 1:
			printnum(temp.charAt(i-1));
			break;
		default:
			break;
		}
		}count--;
	}
}
static void printnum(char x) {
	switch(x) {
	case '1':
		System.out.print("One ");
		break;
	case '2':
		System.out.print("Two ");
		break;
	case '3':
		System.out.print("Three ");
		break;
	case '4':
		System.out.print("Four ");
		break;
	case '5':
		System.out.print("Five ");
		break;
	case '6':
		System.out.print("Six ");
		break;
	case '7':
		System.out.print("Seven ");
		break;
	case '8':
		System.out.print("Eight ");
		break;
	case '9':
		System.out.print("Nine ");
		break;
	default:
		break;
	}
}
static void printtens(char x) {
	switch(x) {
	case '2':
		System.out.print("Twenty ");
		break;
	case '3':
		System.out.print("Thirty ");
		break;
	case '4':
		System.out.print("Forty ");
		break;
	case '5':
		System.out.print("Fifty ");
		break;
	case '6':
		System.out.print("Sixty ");
		break;
	case '7':
		System.out.print("Seventy ");
		break;
	case '8':
		System.out.print("Eighty ");
		break;
	case '9':
		System.out.print("Ninety ");
		break;
	default:
		break;
	}
}
static void printones(char x) {
	switch(x) {
	case '0':
		System.out.print("Ten ");
		break;
	case '1':
		System.out.print("Eleven ");
		break;
	case '2':
		System.out.print("Twelve ");
		break;
	case '3':
		System.out.print("Thirteen ");
		break;
	case '4':
		System.out.print("Fourteen ");
		break;
	case '5':
		System.out.print("Fifteen ");
		break;
	case '6':
		System.out.print("Sixteen ");
		break;
	case '7':
		System.out.print("Seventeen ");
		break;
	case '8':
		System.out.print("Eighteen ");
		break;
	case '9':
		System.out.print("Nineteen ");
		break;
	default:
		break;
	}
}
}
```
Explanation: 
1. Get the number from the user
2. Convert the integer into String and find its length
3. If the number is 0 display Zero
4. Traverse through the characters of the String(using for loop) and print with respect to the positions (with the help of count variable)
5. In order to print one, two etc., a method printnum is there.
6. In order to print tens places ie, twenty, thirty etc., a method printtens is there and if it begins with one, printones is there and count is decremented so that next number is not printed.
7. After each digit is printed, the count is decremented.
8. The methods printtens, printones and printnum are executed using switch case and are in such a way that it will not print 0.
