# Code
```
import java.util.*;

class Main {
    public static int lcm(int a, int b) {
        int temp = a*b;
        temp/=gcd(a,b);
        return temp;
    }
    
    public static int gcd(int a, int b) {
        while(true) {
            int temp=b;
            b=a%b;
            a=temp;
            if(b==0) {
                break;
            }
        }
        return a;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the first number: ");
        int a=sc.nextInt();
        System.out.println("Enter the second number: ");
        int b=sc.nextInt();
        System.out.println("The largest number that completely divides "+a+" and "+b+" is "+gcd(a,b));
        System.out.println("The smallest number that is the product of "+a+" and "+b+" is "+lcm(a,b));
        sc.close();   
    }
}

```

# Explanation
```
1. First the user is asked to enter the two numbers.

2. Largest number that completely divides both numbers is the GCD of the two numbers.

3. Let a and b be the two numbers, to find gcd of a and b, we find remainder of a/b. The values are updated with a = b and b = remainder of a/b. This is repeated until b becomes zero. The value of a when b = 0, is the GCD of a and b.

4. The smallest number that is the product of both numbers is the LCM of the two numbers.

5. Let a and b be the two numbers. To find the LCM of a and b, we use a simple formula: LCM = (a*b) / GCD of a and b.

```
