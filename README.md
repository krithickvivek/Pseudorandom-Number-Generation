# Ex-6-Pseudorandom-Number-Generation
## AIM:

To implement and demonstrate pseudorandom number generation using the standard library.

## DESIGN STEPS:
### Step 1:
Understand the concept of pseudorandom number generation (PRNG).

### Step 2:
Implement the pseudorandom number generation using a programming language and its standard library functions.

### Step 3:
In PRNG, random numbers are generated based on an initial seed value, and the sequence of random numbers follows a deterministic process.
Many programming languages provide built-in functions for generating pseudorandom numbers, such as random() in Python and rand() in C.
These numbers are uniformly distributed within a given range and can be used in various applications such as cryptography, simulations, and games.

The pseudorandom number generation can be represented as:
𝑋𝑛+1=(𝑎𝑋𝑛+𝑐)mod 𝑚 
where 𝑎,𝑐,and 𝑚 are constants and 𝑋𝑛 is the nth number in the sequence.

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
