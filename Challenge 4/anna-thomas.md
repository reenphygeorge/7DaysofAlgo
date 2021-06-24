Code:
```java
import java.util.*;

public class MergeSort{

	public static void main(String[] args){
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the no of elements you want in the array");
		int no=sc.nextInt();
		int num[]=new int[no];
		System.out.println("Enter all the elements");
		for(int i=0;i<no;i++) {
			num[i]=sc.nextInt();
		}
		MergeSort obj=new MergeSort();
		obj.sort(num,0,num.length-1);
		System.out.println("Sorted array:");
		for(int i=0;i<no;i++){
			System.out.println(num[i]);
		}
		sc.close();
	}
	void sort(int a[],int start,int end){
		if(start<end){
			int mid=(start+end)/2;
			sort(a,start,mid);
			sort(a,mid+1,end);
			merge(a,start,mid,end);
		}
	}
	void merge(int a[],int start,int mid,int end){
		int l=mid-start+1;
		int r=end-mid;
		int la[]=new int[l];
		for(int i=0;i<l;i++){
			la[i]=a[start+i];
		}
		int ra[]=new int[r];
		for(int j=0;j<r;j++){
			ra[j]=a[mid+1+j];
		}
		int i=0,j=0;
		int k=start;
		while(i<l&&j<r){
			if(la[i]<=ra[j]){
				a[k]=la[i];
				i++;
			}else{
				a[k]=ra[j];
				j++;
			}k++;
		}
		while(i<l){
			a[k]=la[i];
			i++;
			k++;
		}
		while(j<r){
			a[k]=ra[j];
			j++;
			k++;
		}
	}
}
```
Explanation:
1. Get the number of elements and elements from the user.
2. Create an object in MergeSort and call the sort function.
3. Find the middle term.
4. Call sort method on first half and second half.
5. Divide the 2 halves further until and unless we are left with individual elements then call merge method.
6. In the merge method, compare the elements that are in both left array and right array respectively.
7. After sorting we get the two sorted halves, merge the halves.
8. Print the sorted array.
