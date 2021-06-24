# Code
```
#Python Code
#Problem Statement : Implement a pure function that takes an array of numbers as an argument and return the array sorted. The sorting must be done through the merge sort algorithm
#Author : Akshara Raju

def merge_sort(num_array):
    if len(num_array) == 1:
        return(num_array)
    if len(num_array) > 1:
        flag = 1
        mid_point = len(num_array)//2
        templ = num_array[:mid_point]
        tempr = num_array[mid_point:]
        merge_sort(templ)
        merge_sort(tempr)
        i=0
        j=0
        k=0
        while i < len(templ) and j< len(tempr):
            if templ[i] < tempr[j]:
                num_array[k] = templ[i]
                i+=1
            else:
                num_array[k] = tempr[j]
                j+=1
            k+=1
        while i < len(templ):
            num_array[k] = templ[i]
            i+=1
            k+=1
        while j < len(tempr):
            num_array[k] = tempr[j]
            j+=1
            k+=1
    else:
        flag = 0
    if flag == 1:
        return(num_array)     


limit = int(input("Enter the limit of your array:"))
num_array = []
print("Enter the Numbers to be Sorted:")
for i in range(limit):
    x = int(input())
    num_array.append(x)
print(merge_sort(num_array))   


     


```

# Explanation
The input array is assigned to the list **num_array**. num_array is passed as an argument to the function **merge_sort**. Inside the function the mid point of the array is found and each half portion of the array is assigned to 2 temporary variables **templ** (for left half of array) and **tempr** (for right half of the array).
The merge_sort function is called for each of this temporary arrays until the length of the array is not greater than 1. The elements in these 2 temporary arrays will be compared with each other and sorted according to their values. Finally when all elements are sorted, the new sorted array is returned.
