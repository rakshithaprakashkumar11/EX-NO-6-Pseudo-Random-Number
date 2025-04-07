# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
Start the program and import the required libraries.
Seed the random number generator using the current time(i.e) rand(time(0));
Get the number of randon number to generate.
Pass the value for number of iterations and print the numbers.
End the program.

# PROGRAM:
```
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

    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");

    for (int i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }

    return 0;
}
```

# OUTPUT:
![WhatsApp Image 2025-04-07 at 08 35 10_0214f280](https://github.com/user-attachments/assets/fdb7df05-d49e-4b62-a5b7-5a434f219ec3)


# RESULT:
The program executed successfully.
