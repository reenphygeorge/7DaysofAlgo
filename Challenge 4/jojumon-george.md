# Code

```

 Java 

import java.util.*;

public class MergeSort

{

	static int[]a= new int[20];	static void merge(int A[],int lb,int ub)

	{	

		int mid=0;

		if(lb<ub)

		{

			mid=(lb+ub)/2;

			merge(A,lb,mid);

			merge(A,mid+1,ub);

			mergeSort(A,lb,mid,ub);

		}

	}

	

	static void mergeSort(int a[],int lb,int mid,int ub) 	

	{

		int[]b= new int[ub];

		int i=lb;

		int j=mid+1;

		int k=lb;

		while(i<=mid && i<=ub)

		{

			if(a[i]<=a[j])

			{

				b[k]=a[i];

				i++;k++;

			}

			else

			{

				b[k]=a[j];

				j++;k++;

			}

		}

		if(i>mid)

		{

			while(j<=ub)

			{

				b[k]=a[j];

				j++;k++;

			}

		}

		else

		{

			while(i<=mid)

			{

				b[k]=a[j];

				j++;k++;

			}

		}

		for(k=0;k<ub;k++)

			a[k]=b[i];

	}

	

	public static void main(String[] args)

	{

		Scanner sc= new Scanner(System.in);

		System.out.println("Enter no. of numbers");

		int n= sc.nextInt();

		System.out.println("Enter the numbers");

		for(int i=0;i<n;i++)

			a[i]=sc.nextInt();

		merge(a,0,n);

		for(int i=0;i<n;i++)

			System.out.println(a[i]);

		sc.close();

	}

}

	

```

# Explanation

  The merge function is based on the principle of divide and conquer algorithm where a problem is divided into multiple sub-problems.

Each sub-problem is solved individually and finally, sub-problems are combined to form the final solutions by recursed function, mergeSort.
