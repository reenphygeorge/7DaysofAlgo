### CODE:

```java

/** Challenge 5: Ceaser Cypher 
* 
* @author Alen Thomas Nellary 
*/ 

import java.util.*;

public class CeaserCypher {
	static String encoder(String text, int shift) {
		String encodedString = "";
		int i=0;
		int len = text.length();	
		while(i<len) {
			char character = text.charAt(i);
			if(Character.isUpperCase(character)) {
				char encode = (char)(character + shift);
				if(encode > 'Z') {
					encodedString = encodedString + (char)(character - (26-shift));
				} else {
					encodedString = encodedString + encode;
				}
			}
			else if(Character.isLowerCase(character)) {
				char encode = (char)(character + shift);
				if(encode > 'z') {
					encodedString = encodedString + (char)(character - (26-shift));
				} else {
					encodedString = encodedString + encode;
				}
			} else {
			encodedString = encodedString + character;
			}
			i++;
		} 
		return encodedString;
	}
	
	public static void main(String[] args) {
		String text, encodedString;
		int shift;
		Scanner scanner = new Scanner(System.in);
		System.out.print("Enter the string to be encoded: ");
		text = scanner.nextLine();
		System.out.print("Enter the no. of shifts you want: ");
		shift = scanner.nextInt();
		if(shift < 0) {
			shift = (shift%26)+26;
		} else {
			shift = shift%26;
		}
		encodedString = encoder(text, shift);
		System.out.println(encodedString);
		scanner.close();
	}
}

```



### EXPLANATION:

- In the CeaserCypher class, we have an encoder() function and a main function.
- In the main function, we accept the text and shift needed, from the user.
- If the shift inputted is less than 0 or greater than 26, then we will take modulus and get values from 0 to 26 for shift.
- Then we call the encoder() function and passes text and shift as parameters to it.
- In the encoder() function, we will extract each character from the text and check for uppercase, lowercase and other characters and based on the ASCII table, we perform shift and write the value to encodedString variable.
- If any encoded character is greater than z after shifting the characters, we perform operation to go through a-z.
- Return the encoded string and in the main function, we display it.
