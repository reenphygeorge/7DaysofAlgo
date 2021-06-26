### CODE:
```java
import java.util.Scanner;
public class Ceasor_Cyphor {
public static void main(String [] args) {
  Scanner sc=new Scanner(System.in);
  System.out.println("enter the word");
  String word=sc.nextLine(); 
  String[] letter=word.split("");
  System.out.println("enter the number between 1 to 26");
  int number=sc.nextInt();
  cypher(word,letter,number);
}
public static void cypher(String word,String [] letter,int number) {
  String  array []= {"a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"};
  for(int i=0;i<word.length();i++) {
	  for(int j=0;j<26;j++) {
		  if(letter[i].equals(array[j])) {
			    System.out.print(array[(j+number)%26]);
			    break;
			}	
			if(letter[i].equals(" ")) {
				System.out.print(" ");
				break;
			}
}}}}
```
### EXPLANATION:
User enters the string and selects the shift.
string is stored in a string array letter by letter and passed through cyphor().
there are two for loops and an if condition which checks if the letter is equal to the string array which has alphabets and that index value is added with shift value and its remainder when divided woth 26 is passed as the index of the string array and printed.
