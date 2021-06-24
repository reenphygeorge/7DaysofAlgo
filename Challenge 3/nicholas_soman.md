#CODE
```java
import java.util.*;
class calpow {
	int power(int k) {
		int res=1;
		 while (k!=0) {
		      res*=2;
		      --k;
		    }
		 return res;
	}
}
class binary{
	void bina(long n) {
		decimal r=new decimal();
		long []a=new long[20];
		int i=0,k=1,p=0;
		calpow o=new calpow();
		while (n>0) {
			a[i]=n%10;
		    n=n/10;
		    i++;
		}
		if(a[0]==1) {
			p=1;
		}
		for(int j=1;j<i;j++) {
			if(a[j]==1) {
				int y=o.power(k);
			    p=p+y;
			}
			k++;
		}
		r.deci(p);
	}
}
class decimal{
	void deci(int n) {
		String [] h= {"0","1","2","3","4","5","6","7","8","9","A","B","C","D","E","F"};
		String [] e=new String[10];
		int q=n;
		int r,i=0;
		while(q!=0) {
			r=q%16;
			q=q/16;
			e[i]=h[r];
			i++;
		}
		for(int j=i-1;j>=0;j--) {
		System.out.print(e[j]);
		}
	}
}
public class baseconvertor {
	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		binary b=new binary();
		decimal d=new decimal();
		System.out.println("Enter the base (2 or 10): ");
		int a=s.nextInt();
		System.out.println("Enter the number: ");
		if(a==2) {
			long n=s.nextLong();
			b.bina(n);
		}
		else {
			int n=s.nextInt();
			d.deci(n);
		}
	}
}
```
#EXPLANATION
Decimal to Hex:
Store the entered number in q.
Then divide q/16 and store it in q.
Store the value of q%16 in r an then store it in an array.
Continue this process until q becomes 0.
At the end we end up with an array which contains the different remainders at each iteration.
Then print the array in reverse.
Binary to Hex:
We convert the binary no: into decimal and then then pass it as a parameter to the decimal() function which then converts it into Hex as above.
Split the int into single components and store it in an array.
Multiply by powers of 2(2^0 for lsb and i for msb)  and add them to convert to decimal form.
