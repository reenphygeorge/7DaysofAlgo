# Code
```
def mergeSort(ele):
    if len(ele)>1:
        mid=len(ele)//2
        Left=ele[:mid]
        Right=ele[mid:]
        mergeSort(Left)
        mergeSort(Right)
        i=j=k=0
        while i<len(Left) and j<len(Right):
            if Left[i]<Right[j]:
                ele[k]=Left[i]
                i+=1
            else:
                ele[k]=Right[j]
                j+=1
            k+=1
        while i<len(Left):
            ele[k]=Left[i]
            i+=1
            k+=1
        while j<len(Right):
            ele[k]=Right[j]
            j+=1
            k+=1

print("Enter the elements to be sorted in space separated form")
ele=list(map(int,input().split()))
mergeSort(ele)
string_ele=[str(i) for i in ele]
print("\nThe sorted array is")
print(" ".join(string_ele))
```

# Explanation
In this program the user is asked to enter the elements to be sorted in space separated format which is then converted into integer list. 
The mergeSort function here, uses divide and conquer mechanism ie divides the list of elements into 2 halves such that each element in the list becomes separate. 
After dividing we start to merge each of the separated list by sorting while combining.
In the mergeSort function, we first check whether the len of list is greater than 1. If so, we find the middle index of the list. Then we have two lists Left(conatins the left elements till mid) and 
Right(conatins the elements from mid till end).Then we do recursion on mergeSort so we divide all the left and right elements. After dividing the elements in the array we start combining. 
For combining we implement the while loop. In the loop we are sorting and combining. If any of the list gets over then we come out of the while loop. Next we will directly enter the 
elements of the list that is not yet over.In the end of the program the array is displayed in space separated format.
