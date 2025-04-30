# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM:
#include <stdio.h>
#include <math.h>

// Function to calculate EMI
void calculateEMI(float principal, float rate, int time) {
    float monthlyRate = rate / (12 * 100);  // Convert annual rate to monthly
    int months = time * 12;

    float emi = (principal * monthlyRate * pow(1 + monthlyRate, months)) /
                (pow(1 + monthlyRate, months) - 1);

    printf("Monthly EMI is: %.2f\n", emi);
}

int main() {
    float principal, rate;
    int time;

    // Taking user input
    printf("Enter loan amount (Principal): ");
    scanf("%f", &principal);

    printf("Enter annual interest rate (in %%): ");
    scanf("%f", &rate);

    printf("Enter loan tenure (in years): ");
    scanf("%d", &time);

    // Call the function
    calculateEMI(principal, rate, time);

    return 0;
}


## OUTPUT:
![m11](https://github.com/user-attachments/assets/c943f872-2ec7-461d-a4e7-6a53ce29e880)

## RESULT:
Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM:
#include <stdio.h>

void generateFibonacci(int terms) {
    int a = 0, b = 1, next;

    printf("Fibonacci Series for %d terms:\n", terms);

    for (int i = 1; i <= terms; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }

    printf("\n");
}

int main() {
    int terms = 6;

    generateFibonacci(terms);

    return 0;
}


## OUTPUT:
![m12](https://github.com/user-attachments/assets/ac5a5724-cb3c-4b19-ac1e-01ccadb0bdb5)

## RESULT:
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM:
#include <stdio.h>

int main() {
    int n;

    // Input the number of elements in the array
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n]; // Declare array to hold n elements

    // Input n elements
    printf("Enter the elements:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Print the last element
    printf("The last element of the array is: %d\n", arr[n - 1]);

    return 0;
}


## OUTPUT:
![m13](https://github.com/user-attachments/assets/dc79bfb7-1c86-480a-9d48-dd723e057459)

## RESULT:
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM:
#include <stdio.h>

int main() {
    int n, count = 0;

    // Input the number of elements in the array
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];  // Declare an array to hold n elements

    // Input n elements
    printf("Enter the elements:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Count the positive elements
    for (int i = 0; i < n; i++) {
        if (arr[i] > 0) {
            count++;
        }
    }

    // Print the count of positive elements
    printf("Total number of positive elements: %d\n", count);

    return 0;
}



## OUTPUT:
![m14](https://github.com/user-attachments/assets/16bf657c-2e75-4c09-8f1e-661597f3a389)

## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
#include <stdio.h>

int main() {
    int n;

    // Input the number of elements in the array
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];  // Declare an array to hold n elements

    // Input n elements
    printf("Enter the elements:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Replace even elements with the character 'E' (ASCII value 69)
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            arr[i] = 'E';  // Replace even number with ASCII value of 'E'
        }
    }

    // Output the modified array
    printf("Modified array:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}


## Output:
![m15](https://github.com/user-attachments/assets/f6e900da-f16c-49f1-b55d-25ce95ea8c51)

## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.

