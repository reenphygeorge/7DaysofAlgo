Code
===
```cpp
#include<iostream>
using namespace std;
int merge(int A[],int no1,int B[],int no2, int C[]);
int main()
{
    int A[20],B[20],C[50],no1,no2,no3=0,i;
    cout<<"Enter number of elements in first array: ";
    cin>>no1;
    cout<<"\nEnter elements of first array(ascending): ";
    for(i=0;i<no1;i++)
      cin>>A[i];
    cout<<"\nEnter number of elements in second array: ";
    cin>>no2;

    cout<<"\nEnter elements of second array(descending): ";
    for(int i=0;i<no2;i++)
      cin>>B[i]; 
    merge(A,no1,B,no2,C);
    no3=no1+no2;
    cout<<"\nThe merged sorted array is below..\n";
    for(i=0;i<no3;i++)
    {
        cout<<C[i]<<" ";
    }
    return 0;  
}
int merge(int A[],int no1,int B[],int no2, int C[])
{
  int a,b,c;
  for(a=0,b=-1,c=0;a<no1 && b>=0;)
  {
    if(A[a]<=B[b])
     {
       C[c++]=A[a++];
     }
     else
    { C[c++]=B[b--]; }
  }
  if(a<no1)
  {
    while(a<no1)
      C[c++]=A[a++];
  }
  else
  {
    while(b>=0)
     C[c++]=B[b--];
  }
}
```
Explanation
===
1.Here I used two separate arrays A and B and when it gets sorted and merged,resultant array will have sum of elements in new array.
2.Compare A[0] and B[0].If A[0]<B[0],moves the element to C[0] and pointer is moved into that array.

3.Next compare A[1] and B[0].If B[0],A[1],move B[0] to C[1] and move the pointer to next element in array B.

4.Continuing the above steps.
