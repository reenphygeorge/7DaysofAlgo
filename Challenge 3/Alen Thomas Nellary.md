### CODE:

```java

/** Challenge 3: Base To Hex
* 
* @author Alen Thomas Nellary 
*/

import java.util.*;

public class BaseToHex {
	
	static void binary(long num) {
		long rem, decimal=0, i=1;
		while (num != 0) {
            rem = num % 2;
            decimal = decimal + rem * i;
            i = i * 2;
            num = num / 10;
         }
         decToHexa(decimal);
	}
	
	static void decToHexa(long num) {
		int remainder;
		char [] codes = new char []{'0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'A', 'B', 'C', 'D', 'E', 'F'};
		ArrayList<String> array = new ArrayList<String>();
        while(num != 0) {  
            remainder = (int)num % 16;   
            array.add(codes[remainder]+"");
            num = num/16;  
        }
        int size = array.size();
        System.out.print("Hexadecimal value: ");
        for(int i=size-1; i>=0; i--) {
             System.out.print(array.get(i));
        }
	}
	
	public static void main(String[] args) {
		long num;
		int op;
		Scanner scanner = new Scanner(System.in);
		System.out.println("Enter the option: (Which conversion you want)");
		System.out.print("1. Decimal -> Hexadecimal \n2. Binary -> Hexadecimal: ");
		op = scanner.nextInt();
		System.out.print("Enter a Number: ");
		num = scanner.nextLong();
	    switch(op) {
	    	case 1:
	    	    decToHexa(num);
	    	    break;
	    	case 2:
	    	    binary(num);
	    	    break;
	    	 default:
	    	    System.out.println("Enter a valid Option!!");
	     }
	     scanner.close();
	}
}

```

### EXPLANATION:

- In the BaseToHex class, we have a binary() function, decToHexa() function and a main function.
- In the main function, we accept a number and conversion option from the user.
- If the option selected is decimal to hexadecimal, then we pass the number to decToHexa() function.
- In the decToHexa() function, we have a char array containing 0-9, also A-F for getting the hex values.
- Then we find the remainder and add it to an Arraylist and then divide it by 16. After that we display the converted hexadecimal value.
- If the option selected is binary to hexadecimal, then we pass the user entered number to the binary() function.
- In the binary() function, we convert the binary value to decimal value first by doing certain operations.
- Then we pass this decimal value to the decToHexa() function, where we display the converted hexadecimal value.
