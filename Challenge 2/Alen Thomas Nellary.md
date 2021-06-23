### CODE:

```java


/** Challenge 2: Spell it out
* 
* @author Alen Thomas Nellary
*/

import java.util.*;

public class SpellNumber {
	
	static String convertNumber(int org_no) {
		int num = org_no;
		String [] set1 = new String [] {" ", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine","Ten", "Eleven", "Twelve", "Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen", "Eighteen", "Nineteen"};  

        String [] set2 = new String [] {" ", "ten", "Twenty", "Thirty", "Forty", "Fifty", "Sixty", "Seventy", "Eighty", "Ninety"};  

        String [] set3 = new String [] {"Hundred", "Thousand"};  
    
		ArrayList<Integer> array = new ArrayList<Integer>();
	  do{
           array.add(org_no % 10);
           org_no = org_no / 10;
       } while  (org_no > 0);
       Collections.reverse(array);
       if(num == 0) {
           return "Zero";
       } else if(num < 20) {
           return set1[num];
       } else if(num < 100) {
           return set2[array.get(0)] +" "+set1[array.get(1)];
       } else if(num < 1000) {
            if((num % 100) < 20) {
         	  return set1[array.get(0)] +" "+ set3[0] +" "+ set1[num % 100];
            } else if(num == 100) {
         	  return set1[array.get(0)] +" "+ set3[0];
            } else {
               return set1[array.get(0)] +" "+ set3[0] +" "+ set2[array.get(1)] +" "+set1[array.get(2)];
            }
        } else if(num == 1000) {
         		return set1[array.get(0)] +" "+set3[1];
        } else {
           	return "Not Possible";
        }
	}
	
	public static void main(String[] args) {
		int num;
		Scanner scanner = new Scanner(System.in);
		System.out.print("Enter a whole number (0 - 1000): ");
		num = scanner.nextInt();
		String spell = convertNumber(num);
		System.out.println(spell);
	}
}

```


### EXPLANATION:

- In the SpellNumber class, we have defined the main function and convertNumber() function.
- In the main function, we accept a whole number between 0 and 1000 as input from the user.
- We take this value and pass this as parameter to the checkNumber() function.
- There we defined 3 String arrays to hold different values from 1-19, 20 and so on.
- Defined an Arraylist to hold the entered digits and then reversing it.
- If the number entered is less than 20, and when it is less than 100 and less than 1000, compare the string arrays with the number based on index values and return the values to the main function.
- In the main function, we display the converted value.
