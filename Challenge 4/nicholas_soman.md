### CODE:
```java
import java.util.*;
public class merge_sort {
	void mergesort(int [] a,int lb,int ub) {
		if(lb<ub) {
			int mid=(lb+ub)/2;
			mergesort(a,lb,mid);
			mergesort(a,mid+1,ub);
			merge(a,lb,mid,ub);
		}
	}
	void merge(int [] a,int lb,int mid,int ub) {
		int i=lb,j=mid+1,k=lb;
		int [] b=new int[50];
		while(i<=mid&&j<=ub) {
			if(a[i]<=a[j]) {
				b[k]=a[i];
				i++;
				k++;
			}
			else {
				b[k]=a[j];
				j++;
				k++;
			}
		}
		if(i>mid) {
			while(j<=ub) {
				b[k]=a[j];
				j++;
				k++;
			}
		}
		else {
			while(i<=mid) {
				b[k]=a[i];
				i++;
				k++;
			}
		}
		for(k=lb;k<=ub;k++)
			a[k]=b[k];
	}
	public static void main(String [] args) {
		Scanner s=new Scanner(System.in);
		int [] a=new int[50];
		merge_sort m=new merge_sort();
		System.out.println("Enter the no: of elements: ");
		int n=s.nextInt();
		System.out.println("Enter the elements: ");
		for(int l=0;l<n;l++) {
			a[l]=s.nextInt();
		}
		System.out.println("Array Before Sorting:");
		for(int l=0;l<n;l++) {
			System.out.print(a[l]+" ");
		}
		m.mergesort(a,0,n-1);
		System.out.println("\n"+"Array After Sorting:");
		for(int l=0;l<n;l++) {
			System.out.print(a[l]+" ");
		}
	}
}
```
### EXPLANATION:

- The array is divided into 2: (0-mid) and ((mid+1)-(n-1)) using mersort().
- The merge() function sorts and merges the 2 sub-arrays.
- mergesort() is a recursive function and thus each sub-array is further divided into 2 and continues this process until n sub-arrays are formed.
- The merge() function sorts and merges the last divided sub-array ,then the sub-array from which the last sub-array was divided and continues until we get a single sorted array back. 
