# Code
```cpp

#include<iostream>
using namespace std;

void merge(int a[],int l,int m,int n)
{
    int j=m+1,c[100];
    int k=l,i=l;
    while(i<=m&&j<=n)
    {
        if(a[i]<a[j])
         c[k++]=a[i++];
        else
        c[k++]=a[j++];
    }
    while(i<=m)
    c[k++]=a[i++];
    while(j<=n)
    c[k++]=a[j++];
    for(i=0;i<k;i++)
    a[i]=c[i];    
}
void mergesort(int a[],int l,int n)
{
   int m;
    if(l<n)
    {
        m=(l+n)/2;
        mergesort(a,l,m);
        mergesort(a,m+1,n);
        merge(a,l,m,n);
    }
}

int main()
{
    int n;int a[100];
    cout<<"enter the size of the array:";
    cin>>n;
    cout<<"\nenter the array";
    for(int i=0;i<n;i++)
        cin>>a[i];
    cout<<"\nEntered array :" ;   
    for(int i=0;i<n;i++)
    cout<<a[i]<<" ";   
    mergesort(a,0,n-1);
     cout<<"\n Sorted Array:";
     for(int i=0;i<n;i++)
     cout<<a[i]<<" ";
     return 0;
}
```

# Explanation
**The user is asked to enter the array and its size to be sorted.**

In *mergesort()* recursion feature is implemented and these recursive functions 
including *merge()* gets invoked untill l>n (lowest and highest index of the array).
This is where the elements get broken down to sub elements for both easiness and effectiveness.

In *merge()*,the necessary parameters are passed and it sorts out the sub element 
pairs of the array by comparing,swapping their places and stores in another temporary
array 'c'.Finally all the elements of c[ ] is passed to a[ ] (original array).  
