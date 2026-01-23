**C**

* The pointer is a datatype in which we can store the **base address of the value**. 
* It can be **int, char, array, function or any other pointer**.
* It **points to memory location where the first byte is stored**.
* The size is dependent on the architecture.
* Syntax "*" (asterix symbol).
* The memory is kept reserved when we declare the int or any other data-type as per the size in the architecture.

data_type *pointer_name
eg. int x = 9, *ptr = &x;
    
 The memory will be allocated for the integer that contains value 9. The address of the memory is A1.
 The address value of var will be stored in "*ptr" (pointer variable). The pointer variable will store the address of another pointer. 
 "*" dereference operator (indirection operator) and "&" is the address of operator. 

 Value of operator/ indirection operator/ dereference opereator is an operator that is used to access the value stored at the location pointed by the pointer. 
 eg. int x = 5;		//value of x is 5
 	int *ptr;		//ptr variable which is in an integer
	ptr = &x;		//address of x to variable ptr 
	printf("%d", *ptr); 	//print value 5 (value of operator)

* Segmentation fault - when the code tries to access illegal memory location

* Minimum and Maximum element in the array (make changes and reflect back from function to main)

		#include <stdio.h>

		void min_max (int arr[], int len, int *min, int *max) {
    	*min = *max = arr[0];
    	for(int i=0; i<len; i++) {
        if (arr[i] > *max) 
            *max = arr[i];
        if (arr[i] < *min)
            *min = arr[i];
    		}
		}

		int main() {
		int a[] = {4535,856,325,9986,8346,23,6,34,9,54,5756};
	
		int min, max;
		int len = sizeof(a)/sizeof(a[0]);
		min_max(a, len, &min, &max);
		printf("Minimum value is %d and maximum value is %d", min, max);
		return 0;
    
		}

* The pointers in arrays

        #include <stdio.h>
  
    	int main() {
		int a[] = {11, 12, 13, 14, 15};
		int sum = 0, *p;

    	for(p = &a[0]; p <= &a[4]; p++)
        sum += *p;
        printf("The sum is %d", sum);
		}

  
* Reverse order of array using pointer

c
    
	#include <stdio.h>
	#define N 5
	int main() {
    int a[N], * p;
    printf("Enter %d elements in the array:", N);
    for (p = a; p <= a + N - 1; p++)
        scanf("%d", p);

    printf("Elements in reverse array are:\n");
    for (p = a+N-1; p >= a; p--)
        printf("%d ", *p);

    return 0;
	}

* How to calculate the memory location of a specific item in an array.
-> Find the starting point of the memory addresses, then calculate the number of elements that we have to travel to get to that element.
-> Multiply the number of elements to the size of the data-type.
-> Here the address and the pointer help us as they mark or point data that we want.

Formula 
&a[i][j] = BA + [(i-lb1) x NC + (j-lb2)] x c

BA =  Base Address
NC  =  Number of columns
c = size of data type of elements stored in array (bytes)

lb - lower bound of row/column
ub - upper bound of row/column

For a[40][50]
BA = 0
NC  = 100
c = 1byte (universal assumption)

* Playing with pointer

		#include <stdio.h>

			int main() {
				unsigned int x[4][3] = {{1,2,3}, {4,5,6},
	                        {7,8,9}, {10,11,12}};
	 			printf("The value of (x+3)= %u, *(x+3)= %u, *(x+2)+3 %u", (x+3), *(x+3), *(x+2)+3);
		}

  The output of all these will be same as
  x+3 = pointer of 4th (3) 1D array
  *(x+3) = pointer of the 1st element of the 4th 1D array
  *(x+2) + 3 = pointer to the 1st element of the 3rd 1D array
  


  
