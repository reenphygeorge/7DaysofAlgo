# Code
```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Enter The First Number:");
        Scanner scanner = new Scanner(System.in);
        int firstNumber = scanner.nextInt();
        System.out.println("Enter the Second Number:");
        int secondNumber = scanner.nextInt();
        hcfAndLcm(firstNumber,secondNumber);
    }
    static void hcfAndLcm(int first, int second){
        int temp1 = first;
        int temp2 = second;
        while(temp2 != 0){
            int temp = temp2;
            temp2 = temp1%temp2;
            temp1 = temp;
        }
        int hcf = temp1;
        int lcm = (first*second)/hcf;

        System.out.println("Largest number that completely divides both numbers: "+hcf);
        System.out.println("The smallest number that is the product of both numbers: "+lcm);
    }
}

```

# Explanation
- This code is used to find Largest number that completely divides both numbers and the smallest number that is the product of both numbersm. ie, in simpler terms HCF and LCM of the provided two numbers.
