# Ex-6-Pseudorandom-Number-Generation
## AIM:

To implement and demonstrate pseudorandom number generation using the standard library.

## DESIGN STEPS:
### Step 1:
Get the number of random numbers to generate from the user.

### Step 2:
Get the seed value from the user.

### Step 3:
Initialize the constants for the Linear Congruential Generator (LCG).

### Step 4:
Generate a random number using the seed and the LCG formula.

### Step 5:
Repeat the random number generation for the specified count.

### Step 6:
Print each generated random number.

### Step 7:
End the program.

## PROGRAM:
```
#include <stdio.h>
//Constants for LCG
#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

//Linear Congruential Generator function
unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("*Pseudorandom number generator*\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/67d4f092-e23d-4db6-bcea-dfd1071e4495)


## RESULT:

The program is executed successfully, demonstrating pseudorandom number generation using the standard library functions in C programming.
