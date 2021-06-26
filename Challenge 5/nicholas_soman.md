# CODE
```java
import java.util.*;
public class Ceasercyphor {
	public static void main(String [] args) {
		String [] n1= {"A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"};
		String [] n2={"a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"};
		Scanner s=new Scanner(System.in);
		int [] c=new int [200];
		System.out.println("Enter the string :");
		String a=s.nextLine();
		System.out.println("Enter value of shift(0-25): ");
		int n=s.nextInt();
		String [] b=a.split("");
		System.out.print("Ceasor Cyphor: ");
		for(int i=0;i<a.length();i++) {
			for(int j=0;j<26;j++) {
				if(b[i].equals(n1[j])) {
				    c[i]=(j+n)%26;
				    System.out.print(n1[c[i]]);
				    break;
				}	
				if(b[i].equals(n2[j])) {
				    c[i]=(j+n)%26;
				    System.out.print(n2[c[i]]);
				    break;
				}
				if(b[i].equals(" ")) {
					System.out.print(" ");
					break;
				}
			}
		}
	}
}
```
# EXPLANATION
- We have 2 arrays n1 and n2 containing A-Z and a-z.
- Split the string into the letters using split() and store it in an array.
- Find the corresponding index no: by matching it to either n1 or n2.
- Use the index no: and the mod value to shift towards right mod places using the equation (index+mod)%26.
- Then print the corresponding array value of n1 or n2 by passing (index+mod)%26 as index.
