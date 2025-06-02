

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
//type your code here
```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d) {
    int max = a;
    if (b > max) max = b;
    if (c > max) max = c;
    if (d > max) max = d;
    return max;
}

int main() {
    int n1, n2, n3, n4, greater;
    printf("Enter four numbers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);
    greater = max_of_four(n1, n2, n3, n4);
    printf("The greatest number is: %d\n", greater);
    return 0;
}

```

Output:
//paste your output here
![image](https://github.com/user-attachments/assets/f9bfa7ba-bfaa-4bd6-a69e-a2f1c8aea928)

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
//type your code here
```
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int a = i & j;
            int o = i | j;
            int x = i ^ j;

            if (a < k && a > max_and) max_and = a;
            if (o < k && o > max_or) max_or = o;
            if (x < k && x > max_xor) max_xor = x;
        }
    }

    printf("Maximum AND: %d\n", max_and);
    printf("Maximum OR : %d\n", max_or);
    printf("Maximum XOR: %d\n", max_xor);
}

int main() {
    int n, k;
    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);
    calculate_the_max(n, k);
    return 0;
}

```
Output:
//paste your output here
![image](https://github.com/user-attachments/assets/4cf1bc1a-0972-44bf-b4ec-a6dc64d0b504)

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
//type your code here
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int noshel, noque;
    scanf("%d %d", &noshel, &noque);

    int** shelarr = malloc(noshel * sizeof(int*));
    int* nobookarr = calloc(noshel, sizeof(int));

    for (int i = 0; i < noque; i++) {
        int type, x, y;
        scanf("%d %d %d", &type, &x, &y);

        if (type == 1) {
            nobookarr[x]++;
            shelarr[x] = realloc(shelarr[x], nobookarr[x] * sizeof(int));
            shelarr[x][nobookarr[x] - 1] = y;
        } else if (type == 2) {
            printf("%d\n", shelarr[x][y]);
        } else if (type == 3) {
            printf("%d\n", nobookarr[x]);
        }
    }

    for (int i = 0; i < noshel; i++) {
        free(shelarr[i]);
    }
    free(shelarr);
    free(nobookarr);

    return 0;
}

```
Output:
//paste your output here
![image](https://github.com/user-attachments/assets/8138909f-59fc-41b3-b05e-fdb9b9c76467)


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
//type your code here
```
#include <stdio.h>

int main() {
    int n, sum = 0;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];
    printf("Enter the elements:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }

    printf("Sum of the elements = %d\n", sum);
    return 0;
}

```
Output:
//paste your output here
![image](https://github.com/user-attachments/assets/f5992d86-3774-4920-baf1-7bae8a65d846)

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
//type your code here
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char sentence[200];
    int count = 0, inWord = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    for (int i = 0; sentence[i] != '\0'; i++) {
        if (isspace(sentence[i])) {
            inWord = 0;
        } else if (!inWord) {
            inWord = 1;
            count++;
        }
    }

    printf("Number of words: %d\n", count);
    return 0;
}

```
Output:
//paste your output here
![image](https://github.com/user-attachments/assets/ab8b4ffd-6e7b-4adb-92fc-95bbfd5a31a3)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
