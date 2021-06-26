# Code
```
import java.util.*;

class Main {
    public static String encode(int k, String s) {
        String result="";
        if(k>25) {
            System.out.println("\nShift value should be less or equal to than 25... Try Again");
            return result;
        }
        int len=s.length();
        if(len==0) {
            System.out.println("\nNo string entered... Try Again");
            return result;
        }
        String enc_lower="abcdefghijklmnopqrstuvwxyz";
        String enc_upper="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        for(int i=0;i<len;i++) {
            if(s.charAt(i)>=65 && s.charAt(i)<=90) {
                int temp = enc_upper.indexOf(s.charAt(i));
                temp=((temp+k)%26);
                result=result+(enc_upper.charAt(temp));
            }
            else if(s.charAt(i)>=97 && s.charAt(i)<=122) {
                int temp = enc_lower.indexOf(s.charAt(i));
                temp=((temp+k)%26);
                result=result+(enc_lower.charAt(temp));
            }
            else {
                result=result+(s.charAt(i));
            }
        }
        return result;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the string to be encoded: ");
        String str = sc.nextLine();
        System.out.println("Enter the shift constant: ");
        int k=sc.nextInt();
        String result=encode(k, str);
        System.out.println("Entered String: "+str);
        System.out.println("Encoded String: "+result);
    }
}

```

# Explanation
```
1. First, the user is asked to enter the string to be encoded & the shift constant which denotes the no of places to be shifted.

2. Now the encode() method is called with the String and shift constant as arguments.

3. Inside the encode() method first it's checked whether shift constant is greater than 25 & String length is zero. If it's so then method prints a warning message and returns an empty string. If conditions are false then the main encoding process will start.

4. In the encoding process, two strings enc_lower & enc_upper are initialized with all letters from A-Z. enc_upper has upper case characters, while enc_lower has lower case characters. Another empty String result is initialized for storing the encoded string. 

5. Now the entered string is traversed, and checked whether it is an upper case or lower case alphabet or other characters.

6. If it's other characters then it is concatenated to result string.

7. If it's an upper case alphabet, then the index of that character in the String ' enc_upper ' is found & stored in a variable temp.

8. Now the following operation is performed, temp = temp((temp+k)%26) here k is the shift constant. This is done to find the index of the new character.

9. Now the character at temp is found and is concatenated with the result string.

10. If it was a lower case alphabet, then steps 6,7,8,9 are performed with the String ' enc_lower ' insted of ' enc_upper '.

11. Finally the String is returned and we'll get the required encoded string.

```
