# EX NO: 6 : Pseudo Random Number

## AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

## ALGORITHM:
1. Start the program and import the required libraries.
2. Seed the random number generator using the current time(i.e) rand(time(0));
3. Get the number of randon number to generate.
4. Pass the value for number of iterations and print the numbers.
5. End the program.

## PROGRAM:
```C
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n;

    printf("Enter the seed value : ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate : ");
    scanf("%d", &n);
    printf("Random numbers :\n");

    for (int i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }

    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/a0df672a-b65f-4573-8e6c-f7efd2025ba7)

## RESULT:
Thus, the implementation of Pseudorandom Number Generation Using Standard library is successfully executed.
