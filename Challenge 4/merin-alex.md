## Code: Python3

```python
def mergesort(list1):
    
    if len(list1) < 2:
        return list1

    middle = len(list1)//2
    left = mergesort(list1[:middle])
    right = mergesort(list1[middle:])
    return merge_part(left, right)

def merge_part(left, right):
    
    if not len(left) or not len(right):
        return left or right

    output = []
    i=0
    j=0
    
    while (len(output) < len(left) + len(right)):
        
        if left[i] < right[j]:
            output.append(left[i])
            i+= 1
            
        else:
            output.append(right[j])
            j+= 1
            
        if i == len(left) or j == len(right):
            output.extend(left[i:] or right[j:])
            break 

    return output


list1=list(map(int,input('enter the elements to sort seperated by space ').split()))
print(mergesort(list1))
```
# Code Explanation
As input, we take the a list of seperated integers from users
There are two functions defined: mergesort and merge_part
The mergesort function takes as input the input list to be sorted
This function recursively divides the list (divide and conquer techinique) till a single element (a single element is sorted)is present in the list
The function returns the list until when the length of the list is less than 1

Next phase is merging, the merge_part function takes as input the left list and right listt(left and right list are themselves are sorted initially as a single element) which were created
as part of the splitting process in the above recursive call, and the elements of left and right lists are compared
and based on the comparison the smallest element among them is appended to a new list called `output`.

the process is continued till either the left or right list get finished and if any elements remains 
in any of the list it is appended to the `output`



