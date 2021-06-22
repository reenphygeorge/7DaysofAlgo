# Code
```
import java.util.*;

public class Main
{
	public static int digits(int n) {
	    int count=0;
	    while(n!=0) {
	        count++;
	        n/=10;
	    }
	    return count;
	}
	
	public static String ones(int n) {
	    
	    String str="";
	    switch (n) {
        case 1:
            str="one ";
            break;
        case 2:
            str="two ";
            break;
        case 3:
            str="three ";
            break;
        case 4:
            str="four ";
            break;
        case 5:
            str="five ";
            break;
        case 6:
            str="six ";
            break;
        case 7:
            str="seven ";
            break;
        case 8:
            str="eight ";
            break;
        case 9:
            str="nine ";
            break;
	    }
	    return str;
	}
	
	public static String tens_one(int n) {
	    
	    String str="";
	    switch (n) {
	    case 0:
	        str="ten ";
	        break;
        case 1:
            str="eleven ";
            break;
        case 2:
            str="twelve ";
            break;
        case 3:
            str="thirteen ";
            break;
        case 4:
            str="fourteen ";
            break;
        case 5:
            str="fifteen ";
            break;
        case 6:
            str="sixteen ";
            break;
        case 7:
            str="seventeen ";
            break;
        case 8:
            str="eighteen ";
            break;
        case 9:
            str="nineteen ";
            break;
	    }
	    return str;
	}
	
	public static String tens(int n) {
	    
	    String str="";
	    switch (n) {
        case 2:
            str="twenty ";
            break;
        case 3:
            str="thirty ";
            break;
        case 4:
            str="forty ";
            break;
        case 5:
            str="fifty ";
            break;
        case 6:
            str="sixty ";
            break;
        case 7:
            str="seventy ";
            break;
        case 8:
            str="eighty ";
            break;
        case 9:
            str="ninety ";
            break;
	    }
	    return str;
	}
	
	public static String hunds(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str = ones(n);
	    str=str+"hundred ";
	    return str;
	}
	
	public static String thous(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str = ones(n);
	    str=str+"thousand ";
	    return str;
	}
	
	public static String ten_thous(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str="";
	    if(((n/10)%10)==1) {
	        str=tens_one(n%10)+"thousand ";
	    }
	    else {
	        str=tens((n/10)%10)+ones(n%10)+"thousand ";
	    }
	    return str;
	}
	
	public static String lakhs(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str = ones(n)+"lakh ";
	    return str;
	}
	
	public static String ten_lakhs(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str="";
	    if(((n/10)%10)==1) {
	        str=tens_one(n%10)+"lakh ";
	    }
	    else {
	        str=tens((n/10)%10)+ones(n%10)+"lakh ";
	    }
	    return str;
	}
	
	public static String cr(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str = ones(n)+"crore ";
	    return str;
	}
	
	public static String ten_cr(int n) {
	    if(n==0) {
	        return "";
	    }
	    String str="";
	    if(((n/10)%10)==1) {
	        str=tens_one(n%10)+"crore ";
	    }
	    else {
	        str=tens((n/10)%10)+ones(n%10)+"crore ";
	    }
	    return str;
	}
	
	public static void main (String[] args) throws java.lang.Exception
	{
		Scanner sc = new Scanner(System.in);
		int n=sc.nextInt();
		int temp=n;
		String no = "";
		if(n==0) {
		    System.out.println("zero");
		}
		else {
		    int len=digits(n);
		    for(int i=1;i<=len;i++) {
		        if(len>1&&((temp/10)%10)==1&&i==1) {
		            no=tens_one(temp%10);
		            i++;
		            temp/=10;
		        }
		        else if(i==1) {
		            no=ones(temp%10);
		        }
		        else if(i==2) {
		            no=tens(temp%10)+no;
		        }
		        else if(i==3) {
		            no=hunds(temp%10)+no;
		        }
		        else if(len>=5&&i==4) {
		            continue;
		        }
		        else if(i==4) {
		            no=thous(temp%10)+no;
		        }
		        else if(i==5) {
		            no=ten_thous(n/1000)+no;
		            temp/=10;
		        }
		        else if(len>=7&&i==6) {
		            continue;
		        }
		        else if(i==6) {
		            no=lakhs(temp%10)+no;
		        }
		        else if(i==7) {
		            no=ten_lakhs(n/100000)+no;
		            temp/=10;
		        }
		        else if(len>=9&&i==8) {
		            continue;
		        }
		        else if(i==8) {
		            no=cr(temp%10)+no;
		        }
		        else if(i==9) {
		            no=ten_cr(n/10000000)+no;
		            temp/=10;
		        }
		        temp/=10;
		    }
		}
		System.out.println(no);
	}
}


```

# Explanation

## Functions Used

	1. digits(int n): 
		
		Takes the entered number as argument & returns count of number of digits in the given number.

	2. ones(int n):

		Takes digit in the unit place of the entered number as argument & returns the digit in words.
		For example: ones(3) will return 'three'.

	3. tens(int n):

		Takes digit in the tens place of the entered number as argument & returns it in words.
		For example: tens(7) will return seventy.

	4. tens_one(int n):

		Numbers from 10 to 19 can't be generalised like other 2-digit numbers.
		For example: 22 is spelt twenty two and 29 is spelt twenty nine. Here twenty is common so numbers from 20 to 29 can be genralised. But 12 is spelt twelve and 19 as nineteen. There is'nt anything common between them. So they can't be generalised.

		tens_one(int n) is created to overcome this problem.

		This function is only called when tens place digit is one.
		It takes the digit in the unit place and returns corresponding number.
		For example: tens_one(6) will return sixteen.

	5. hunds(int n):

		Takes the digit in 100th place of number & returns the number in words.
		Actually it calls ones(int n) function and passes the 100th place digit itself as the argument to the function and concatenate the string "hundred" at the end.
		For example we spell 200 as two hundred. Here two is returned by the ones() function and hundred is concatenated at the end.

		If digit at 100th place is 0 (in case of 2021), hunds() will return an empty string.

		thous(), lakhs(), cr() also works in the same way by taking digit in the corresponding place.

	6. ten_thous(int n):

		12000 is spelt twelve thousand.
		If we had used thous() function we would've got one thousand two thousand 😂

		So to solve this issue, ten_thous() function is used.

		Unlike other functions, it takes digits in both 1000th and 10000th place as a single number.
		For example: if n=27576, the function would take 27 as the argument.

		Inside the function, it would split the number into ones place and tens place digits.
		If digit in the tens place is 1 then function tens_one() will be called with the number itself as the argument.
		Else tens() and ones() functions will be called with tens and ones place digits as the respective argument.
		The strings returned from both the function will be concatenated with the string "thousand" and returned.

		Also if this function is caled, then thous() function will not be called for 1000th place digit.
		This is done to avoid situations like one thousand two thousand 😂

		ten_lakhs() & ten_cr() functions also works in the same way with the corresponding arguments.
	
## Working

	1. Number of digits is calculated by using digits() function.

	2. An empty string is initialized.

	3. Each digit of the number is traversed with the help of a loop from 1 to total number of digits, and are passed into the corresponding functions.

	4. Strings returned from the functions will be concatenated with the above initialized string.

	5. Finally we will get the required string containing the entered number in words.