# Code
```
#include <stdio.h>
#include <stdbool.h>

bool IsPrime (int num){
    int a=num;
		int flag=0;
		for(int i=2;i<=a/2;i++) {
			if (a%i==0) 
				flag=1;
		}
		if (flag==0) {
			return true;
		}
		else 
			return false;
}
int main() {
  int n;
  printf("Enter a natural number: ");
  scanf("%d",&n);
	if(IsPrime(n))
    printf("TRUE");
  else
    printf("FALSE");
  return 0;
}

```

# Explanation
1. Get number from the user
2. Check whether its 0 or 1 and if yes Error.
3. To check whether its prime, the divisibility of the number(n) with numbers from 2 to n/2 is checked (using for loop) as the numbers after n/2 will be divisible by those before n/2.
4. Using a variable flag, if it is divisible by any number then flag= 1 else 0.
5. Using bool function if flag is 0, it will return true else false and we can determine whether it is prime (TRUE) or not (FALSE).

