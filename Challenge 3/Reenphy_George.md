# Code
```
import java.util.*;

class Main {
    
    public static String tohex(int n) {
        char[] hexa = {'0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F'};
        Stack<Integer>stk = new Stack();
        String result = "";
        while(n!=0) {
            stk.push(n%16);
            n/=16;
        }
        while(stk.isEmpty()!=true) {
             result=result+hexa[stk.pop()];
        }
        return result;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        System.out.println(tohex(n));    
    }
}

```

# Explanation

## Functions Used
- tohex(int n) takes an integer as argument & resturns it's hexadecimal equivalent.

## Initialization
- A character array hexa[] is initialized with hexa decimal values corresponding to the array indices.
- A stack of Integer type is initialized for storing the reminders.
- An empty string result is initialized for storing the final hexadecimal value.

## Working
1. Reminder of  n / 16  is pushed into the stack.
2. Value of n is updated as n = n / 16.
3. Steps 1 & 2 are repeated until n becomes zero.
4. Now the stack is poped.
5. After each pop operation, the hexadecimal equivalent of poped number is obtained from the character array hexa[].
6. The string obtained from the array hexa[] is concatenated with the String result.
7. Steps 4, 5, 6 are repeated until the stack becomes empty.
8. Thus we get the hexadecimal equivalent of entered whole number.