### CODE:

```java

/** Challenge 4: Sort Me 
* 
* @author Alen Thomas Nellary 
*/

import java.util.Scanner;

public class SortArray {
        static void merge_sort(int [] org_array, int first, int mid, int last) {
        int x =0, y = 0, i= 0, j = 0, n1, n2;
        n1 = mid - first + 1;
        n2 = last - mid;
        
        int [] left_array = new int [n1];
        int [] right_array = new int [n2];
        
        while(x < n1) {
        	left_array[x] = org_array[first + x];
        	x++;
        }
        
        while(y < n2) {
        	right_array[y] = org_array[mid + 1+ y];
        	y++;
        }

        while (i < n1 && j < n2) {
             if (left_array[i] <= right_array[j]) {
                org_array[first] = left_array[i];
                i++;
             } else {
                org_array[first] = right_array[j];
                j++;
             }
             first++;
        }

        while (i < n1) {
            org_array[first] = left_array[i];
            i++;
            first++;
        }

        while (j < n2) {
            org_array[first] = right_array[j];
            j++;
            first++;
        }
    }
    
    static void sort_array(int [] org_array, int start, int end) {
         if (end > start) {
             sort_array(org_array, start, (start + end)/2);
             sort_array(org_array, ((start+end)/2)+1, end);
             merge_sort(org_array, start, (start+end)/2, end);
          }
        }

    public static void main(String args[]) {
    	int num, len;
    	Scanner scanner = new Scanner(System.in);
    	System.out.print("Enter the number of elements: ");
    	num = scanner.nextInt();
    	int [] array = new int[num];
    	System.out.print("Enter the elements in the array: ");
    	for(int i=0; i<num; i++) {
    		array[i] = scanner.nextInt();
    	}
    	len = array.length;
        System.out.print("Array Before Sorting: ");
        for (int i=0; i<num; ++i) {
            System.out.print(array[i] + " ");
        }
        System.out.println();
        sort_array(array, 0, len-1);
        System.out.print("Array After Sorting: ");
        for (int i=0; i<num; ++i) {
            System.out.print(array[i] + " ");
        }
        System.out.println();
     }
}

```


### EXPLANATION:

- In the SortArray class, we have defined a merge_sort() function, sort_array() function and also there is a main function.
- In the main function, we first accept the number of elements in the array and we run a for loop to insert each element entered by the user into the array.
- Then we display the original unsorted array.
- After that we pass the orginal array along with the start and end elements as parameters to the sort_array() function.
- Then we run a recursive function to call the sort_array() again. After that we call the merge_sort() function by passing the array along with first, middle, and last elements as parameters.
- In the merge_sort() function, we divide the main array into two subarrays based on the middle element.
- Then we will sort the first array ie., left_array and also sort the second array ie., right_array.
- After that we will merge the two sorted subarrays.
- Then display the sorted array.
