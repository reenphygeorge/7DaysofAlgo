### CODE:

```java

/** Challenge 7: Factors and Multiples
* 
* @author Alen Thomas Nellary 
*/ 


import java.util.Scanner;

public class FactorMultiple {
	
	static int hcf(int num1, int num2) {
		int i=1, hcf =1;
		while(i <= num1 && i <= num2) {
			if(num1%i == 0 && num2%i == 0) {
				hcf = i;
			}
            i++;
        }
        return hcf;
	}
	
	static int lcm(int num1, int num2, int hcf) {
		int lcm = (num1 * num2) / hcf;
		return lcm;
	}
	
	public static void main(String [] args) {
		int num1, num2;
		Scanner scanner = new Scanner(System.in);
		System.out.print("Enter the first number: ");
		num1 = scanner.nextInt();
		System.out.print("Enter the second number: ");
		num2 = scanner.nextInt();
		int hcf = hcf(num1, num2);
		int lcm = lcm(num1, num2, hcf);
		System.out.print("HCF: "+hcf+"\nLCM: "+lcm);
		scanner.close();
	}
}

```


### EXPLANATION:

- In the FactorMultiple class, we have a hcf() function, lcm() function, and a main function.
- In the main function we accept two numbers and then call hcf() and lcm() functions and pass the numbers as parameters and hcf as extra parameter to the lcm() function.
- In the hcf() function, initialise i and hcf as 1. Then run a while loop till i less than or equal to num1 and num2.
- If the modulus of num1 and num2 with i equals 0, then assign hcf variable with i. Then increment the value of i and finally return hcf.
- In the lcm() function, assign (num1*num2) / hcf to lcm and return lcm.
- In the main function, we display the returned values as HCF and LCM.
