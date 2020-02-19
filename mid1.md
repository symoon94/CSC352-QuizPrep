LONG ANSWER:

1) Why doesn't sizeof() represent of the size of an array?

	- sizeof operator is basically used when actual size of the object must be known. 

	- It returns the size, in bytes, of the object representation of "type".

	- Depending on the computer architecture, a byte may consist of 8 or more bits, the exact number provided as CHAR_BIT.

	- So, if you want to find the length of an array in C, the method would be like below:

	int main(void) {
		
		int a[] = {1,2,3,4};
		int size;

		size = sizeof(a)/sizeof(a[0]);  // Method

		printf ("size = %d", size);

		return 0;

	}


2) Why does each data type of int require different amounts of memory in C?

	- due to when c was made because back then, the size of the bit in the computer was inconsistent.

	- they started it off with 16bit CPU and CPU became 32, and it became 64. So originally in 16bit CPU short was 16, int was 16, and long was 32 

	- Because the CPU handles a bit differently, 64bit CPU's short became 16, int 32, and long 64. 
	
	- running 64 bit on 32 but makes it run slower because 32 bit have to add to become 64 bit.