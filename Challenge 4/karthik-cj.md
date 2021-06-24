### CODE:

```java

/** Challenge 4: Sort Me
* 
* @author Karthik._.cj
*/

import java.util.*;
class MergeSort
{
    static void printArray(Integer[] arr)
    {
        int size = arr.length;
        for (int i = 0; i < size; ++i)
            System.out.print(arr[i] + " ");
                System.out.println();
    }

    void mergesort(Integer[] arr , int first , int mid , int last)
    {
        int len1 = mid - first + 1;
            int len2 = last - mid;

        int Left[] = new int[len1];
            int Right[] = new int[len2];
 
        for (int i = 0; i < len1; ++i)
            Left[i] = arr[first + i];
                for (int j = 0; j < len2; ++j)
                     Right[j] = arr[mid + 1 + j];

        int i = 0, j = 0;
 
        int k = first;
             while (i < len1 && j < len2) {
                if (Left[i] <= Right[j]) {
                    arr[k] = Left[i];
                         i++;
            }
            else 
            {
                arr[k] = Right[j];
                    j++;
            }
                k++;
        }
 
        while (i < len1) 
        {
            arr[k] = Left[i];
                i++;
                    k++;
        }
 
        while (j < len2) 
        {
            arr[k] = Right[j];
                j++;
                    k++;
        }
    }
 
    void sortArray(Integer[] arr, int first, int last)
    {
        if (first < last) {
            int mid = first + (last - first) / 2; 

            sortArray(arr, first , mid);
                sortArray(arr , mid + 1 , last);
                    mergesort(arr , first , mid , last);
        }
    }
 
    public static void main(String args[])
    {
        MergeSort sort = new MergeSort();
            Scanner sc = new Scanner(System.in);
                System.out.print("\nEnter the size of the array : ");
                     int size = sc.nextInt();

        Integer[] arr = new Integer[size]; 
             System.out.print("\nEnter the elements : ");
                for(int i = 0 ; i < size ; i++)
             {
                 arr[i] = sc.nextInt();
             }

        System.out.println("\nUnsorted array : ");     
          printArray(arr);
             sort.sortArray(arr, 0, arr.length - 1);
                System.out.println("\nSorted array : ");
                    printArray(arr);

        sc.close();
    }
}

```

### EXPLANATION:

- User Enters the elements of array in unsorted order.
- Print function is invoked and unsorted array is printed.
- An object of MergeSort class is created and sortArray method is invoked with corresponding parameters.
- Mid value is then calculated and a recursive function is called twice.
- Then mergesort method is called with parameters.
- There the lenght of splitted array is calculated , and two arrays are created.
- Then the algorithm of Left and Right arrays are implemented.
- And two while loops are created for each Arrays and Sorted Array is printed.

  THANK YOU
