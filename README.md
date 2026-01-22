# Fundamentals-of-C-C-Python
Practicing and learning few fundamental concepts of C/C++/Python

--
**  C  **

* The pointer is a datatype in which we can store the address of the value. 
* It can be int, char, array, function or any other pointer.
* The size is dependent on the architecture.
* Syntax "*" (asterix symbol).
* The memory is kept reserved when we declare the int or any other data-type as per the size in the architecture.

eg. int var = 9;
    int *ptr = &var;
    
 The memory will be allocated for the integer that contains value 7. The address of the memory is A1.
 The address value of var will be stored in "*ptr" (pointer variable). The pointer variable will store the address of another pointer. 
 "*" dereference operator (indirection operator) and "&" is the address of operator. 

* The pointers in arrays

'''
#include <stdio.h>

int main() {
	int a[] = {11, 12, 13, 14, 15};
	int sum = 0, *p;
	
    for(p = &a[0]; p <= &a[4]; p++)
        sum += *p;
        printf("The sum is %d", sum);
}
'''

