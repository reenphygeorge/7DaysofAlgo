Code
```java
import java.util.Scanner;

public class CaesarCipher {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the string to be encrypted");
		String text=sc.nextLine();
		System.out.println("Enter the shift:");
		int shift=sc.nextInt();
		if(shift>26) {
			shift=shift%26;
		}else if(shift<0) {
			shift=(shift%26)+26;
		}
		System.out.println("Encrypted text:");
		System.out.println(encrypt(text,shift));
		sc.close();
	}
	public static String encrypt(String str,int x) {
		String encrypted="";
		for(int i=0;i<str.length();i++) {
			char add=str.charAt(i);
			if(Character.isAlphabetic(add)) {
				if(Character.isUpperCase(add)) {
					char a=(char)(add+x);
					if(a>'Z') {
						encrypted+=(char)(add-(26-x));
					}else {
						encrypted+=a;
					}
				}else if(Character.isLowerCase(add)) {
					char a=(char)(add+x);
					if(a>'z') {
						encrypted+=(char)(add-(26-x));
					}else {
						encrypted+=a;
					}
				}
			}else {
				encrypted+=add;
			}
		}
		return encrypted;
	}
}
```
Explanation:
1. Get the string to be encrypted and the shift from the user.
2. Make the shift in such a way that it is between 0 and 25.
3. Call a method encrypt which returns encrypted text.
4. Separate each characters in the text given and check whether its in Upper Case, Lower Case, Symbols or Spaces.
5. Add the characters to the encrypted text and if the encrypted character's value in Upper Case or Lower Case goes more than Z/z, start it again starting from A/a.
6. Display the encrypted text.
