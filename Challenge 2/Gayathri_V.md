# Code
```
/*
Author : Gayathri V
Challenge 2: Spell it out.
*/



import java.util.Scanner;

public class NumAsWord {

    static String toWord(int number) {

        String word = "";

        String[] wordArray1 = new String[]{" One", " Two", " Three", " Four", " Five", " Six", " Seven", " Eight", " Nine"};
        String[] wordArray2 = new String[]{" Eleven", " Twelve", " Thirteen", " Fourteen", "Fifteen", " Sixteen", " Seventeen", " Eighteen", " Nineteen"};
        String[] wordArray3 = new String[]{" Twenty", " Thirty", " Fourty", " Fifty", " Sixty", " Seventy", " Eighty", " Ninety"};


        int num;
        int index;

        /* 0 10 100 have unique names, not required further */

        if (number == 0) {
            word = "Zero";
        } else if (number == 10) {
            word = "Ten";
        } else if (number == 100) {
            word = "Hundred";
        } 


          else if (number > 0 && number < 10) {  //one digit[unique names]
            num = 1;
            index = 0;
            while (number != num) {
                if (num != 9) {
                    num++;
                    index++;
                }
            }
            word = wordArray1[index];


        } else if (number > 10 && number < 20) { // two digits[unique names]
            num = 11;
            index = 0;
            while (number != num) {
                if (num != 19) {
                    num++;
                    index++;
                }
            }
            word = wordArray2[index];


        } else if (number % 10 == 0 && number > 0 && number < 101) {  //multiple of 10 [unique names]
            num = 20;
            index = 0;
            while (number != num) {
                if (num != 100) {
                    num = num + 10;
                    index++;
                }
            }
            word = wordArray3[index];


        } else if (number > 100 || number < 0) {
            System.out.println("Enter your integer Number between 0 and 100.");
            word = "unknown";

        } else if (number > 19 && number % 10 != 0) { // 2 digit not multiple of 10 [ names can be derived like Twenty Two ,Thirty Four  etc..]

            int array[][] = new int[8][9];
            int i, j = 0;
            num = 21;


            for (i = 0; i < 8; i++) {
                for (j = 0; j < 9; j++) {
                    if (num != 100){
                        array[i][j] = num;
                        num++;                   //assigning numbers to array from 21 to 99
                        if (num % 10 == 0) {       // excluding multiple of 10,already checked
                            num++;
                        }
                    }
                }
            }

            for (i = 0; i < 8; i++) {
                for (j = 0; j < 9; j++) {
                    if (number == array[i][j]) {
                        word = wordArray3[i] + wordArray1[j];
                        break;
                    }
                }
            }

        }
        return word;
    }
    public static void main(String[] args){

       Scanner scanner = new Scanner(System.in);

        System.out.println("Hey!!.Please Enter your integer Number between 0 and 100.");
        int number = scanner.nextInt();

        String word = toWord(number);
        System.out.println("The number \""+number + "\" in word is \""+word +"\"");

    }
}

```

# Explanation
In the Main method user can enter any number between 0 and 100.
The "toWord" method will able to perform the operations.
Since the 1 to 10 and 11 to 19 , also 10,20....90 have unique names they printed separatly.
Each of them have string array to store their names.
For the other cases , a multi dimensional array to store numbers used and entered number is checked.
The index of this array will be equal to the index of two separate String arrays which contains the names of 10, 20..90 and 1, 2...9.
Hence obtained names will be returned to main and printed.
Program terminates.

