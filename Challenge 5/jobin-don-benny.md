CODE:
```java

import java.util.Scanner;
public class Cipher { //Section 1
    static final Scanner scanner = new Scanner(System.in);
    public static final String myAlphabets = "abcdefghijklmnopqrstuvwxyz";
    public static void main(String[] args) {
        System.out.println("Enter the String/Message:");
        String message = scanner.nextLine();
        System.out.println(encode(message));
    }
    static String encode(String message){ //Section 2
        System.out.println("Enter the Key");
        int key = scanner.nextInt();
        message = message.toLowerCase();
        StringBuilder cipherText = new StringBuilder();
        for (int j = 0; j< message.length(); j++){
            int myPosition = myAlphabets.indexOf(message.charAt(j));
            int myKeyValue = (key + myPosition) % 26;
            char myValues = myAlphabets.charAt(myKeyValue);
            cipherText.append(myValues);
        }
        return cipherText.toString();

    }
}
```
EXPLANATION:

- Caesar's cipher is a type of substitution cypher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.
- In this code Section 1 is where we accept the String to be encoded from the user and the String "myAlphabets" which has the letters from a to z is defined.
- In Section 2 we obatain  the Key(The actual number of places the characters in the string needs to be shifted) from the user.
- In the for() loop we shift the the letters and append the newly created string to "cipherText".
- The encoded message is returned back to the main() method as a string. 
- NOTE: If the user provided string contains spaces or special characters(@,#,$..), then in the encoded message these places will have the value of the entry in myAlphabets wrt the key provided by the user. For example if the key value is 3, then the places where there are spaces or special characters will have the character "c" which is the third character in the string "myAlphabets" after encoding. It can either be considered a feature or a bug depending on how you look at it ;)
