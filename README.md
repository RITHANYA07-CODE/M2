# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:

```c
#include <stdio.h>

int main() {
    int M, N;

    // Getting user input
    printf("Enter the values of M and N: ");
    scanf("%d %d", &M, &N);

    printf("Even numbers from %d to %d are:\n", M, N);

    // Adjust M if it's odd to start from the next even number
    if (M % 2 != 0) {
        M++;  
    }

    // Loop to print even numbers
    for (int i = M; i <= N; i += 2) {
        printf("%d ", i);
    }

    printf("\n"); // New line for clean output
    return 0;
}
```

## OUTPUT:
Enter the values of M and N: 10 20
Even numbers from 10 to 20 are:
10 12 14 16 18 20 

## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 
# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:


## OUTPUT:
![image](https://github.com/user-attachments/assets/1c7ec586-a0ef-4e16-a303-48cd2f2e99c9)





## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 

# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:

```c
#include <stdio.h>

// Function to perform addition
void add(int a, int b) {
    int sum = a + b;
    printf("Addition of %d and %d is: %d\n", a, b, sum);
}

// Function to perform subtraction
void subtract(int a, int b) {
    int diff = a - b;
    printf("Subtraction of %d and %d is: %d\n", a, b, diff);
}

int main() {
    int num1, num2;

    // Getting user input
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Function calls
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}
```

## OUTPUT:
Enter two numbers: 2 3
Addition of 2 and 3 is: 5
Subtraction of 2 and 3 is: -1

## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 
# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:

```c
#include <stdio.h>

int main() {
    int num, digit, sum = 0;

    // Getting user input
    printf("Enter a number: ");
    scanf("%d", &num);

    // Using a for loop to extract and check digits
    for (; num > 0; num /= 10) {
        digit = num % 10;  // Extract the last digit

        if (digit % 2 != 0) {  // Check if digit is odd
            sum += digit;      // Add to sum if odd
        }
    }

    // Printing the result
    printf("Sum of odd digits is: %d\n", sum);

    return 0;
}
```

## OUTPUT:
Enter a number: 123456789
Sum of odd digits is: 25

## RESULT:
Thus the program to find the sum of odd digits using for loop has been executed successfully.


# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:

```c
#include <stdio.h>

// Function to calculate factorial
void fact() {
    int i, N;
    unsigned long long factorial = 1; // Using long long to handle large factorials

    // Getting user input
    printf("Enter a number to find its factorial: ");
    scanf("%d", &N);

    if (N < 0) {
        printf("Factorial of a negative number doesn't exist.\n");
        return;
    }

    // Calculating factorial using for loop
    for (i = 1; i <= N; i++) {
        factorial *= i;
    }

    // Printing the result
    printf("Factorial of %d is: %llu\n", N, factorial);
}

int main() {
    fact();  // Function call
    return 0;
}
```

## OUTPUT:
Enter a number to find its factorial: 5
Factorial of 5 is: 120

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
