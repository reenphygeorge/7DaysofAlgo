### code
```java
import java.util.Scanner;
public class merge_sort {
public static void main(String[] args) {
  Scanner sc=new Scanner(System.in);
  int[] array1 =new int[30];
  System.out.println("enter the number of elements to sort");
  int n=sc.nextInt();
  System.out.println("enter the numbers");
  for(int i=0;i<n;i++) {
    array1[i]=sc.nextInt();
  }
  merge_sort m=new merge_sort();
  m.mergesort(array1,0,n-1);
  System.out.println("array after sorting is");
  for(int i=0;i<n;i++) {
    System.out.print(array1[i]+" ");
  }
}
void mergesort(int array1[],int a,int b) { 
    if(a<b) {
      int mid=(a+b)/2;
      mergesort(array1,a,mid);
      mergesort(array1,mid+1,b); 
      sort(array1,a,mid,b);
    }
  }
  void sort(int array1[],int x,int y,int z) {
    int i=x;
    int j=y+1;
    int k=x; 
    int [] array2=new int[50];
    while(i<=y&&j<=z) {
      if(array1[i]<=array1[j]) {
        array2[k]=array1[i];
        i++;
        k++;
      }
      else {
        array2[k]=array1[j];
        j++;
        k++;
      }
    }
    if(i>y) {
      while(j<=z) {
        array2[k]=array1[j];
        j++;
        k++;
      }
    }
    else {
      while(i<=y) {
        array2[k]=array1[i];
        i++;
        k++;
      }
    }
    for(k=x;k<=z;k++)
      array1[k]=array2[k];
  }
}






### explanation

In this algorithm we are going to sort numbers in that array by merge sort.
  Merge sort is by divide and conquer rule.We need two functions for this ,
one is mergesort and sort, 
in merge sort we are recursively calling the mergesort with first element and last element.
  Mergsort first elemnt and middle element the by middle +1 element and last element ,
continuing this manner ,and giving the array first element middle element and last element to the sort function thus getting the sorted array.
  
