# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	int main() {
	    int length, breadth;
	    int *x, *y;
	    int area;
	
	    // Step 2: Read length and breadth
	    printf("Enter length of rectangle: ");
	    scanf("%d", &length);
	
	    printf("Enter breadth of rectangle: ");
	    scanf("%d", &breadth);
	
	    // Assign pointers
	    x = &length;
	    y = &breadth;
	
	    // Step 3: Calculate area using pointers
	    area = (*x) * (*y);
	
	    // Step 4: Display result
	    printf("Area of rectangle = %d\n", area);
	
	    return 0;
	}


## OUTPUT
Enter length of rectangle: 10
Enter breadth of rectangle: 5
Area of rectangle = 50


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
	#include <stdio.h>
	#include <stdlib.h>
	#include <string.h>
	
	int main() {
	    char *str;
	
	    // Step 2: Allocate memory to hold "WELCOME" plus null terminator
	    str = (char *)malloc(8 * sizeof(char)); // 7 chars + 1 for '\0'
	
	    if (str == NULL) {
	        printf("Memory allocation failed.\n");
	        return 1;
	    }
	
	    // Step 3: Copy string "WELCOME" into allocated memory
	    strcpy(str, "WELCOME");
	
	    // Step 4: Display the string
	    printf("%s\n", str);
	
	    // Step 5: Free allocated memory
	    free(str);
	
	    return 0;
	}

## OUTPUT
WELCOME



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	// Step 2: Define the student structure
	struct student {
	    char name[50];
	    int roll;
	    float marks;
	};
	
	int main() {
	    struct student s1;
	
	    // Step 3: Read student information
	    printf("Enter student name: ");
	    fgets(s1.name, sizeof(s1.name), stdin);
	    
	    printf("Enter roll number: ");
	    scanf("%d", &s1.roll);
	
	    printf("Enter marks: ");
	    scanf("%f", &s1.marks);
	
	    // Step 5: Display student information
	    printf("\nStudent Information:\n");
	    printf("Name      : %s", s1.name);
	    printf("Roll No.  : %d\n", s1.roll);
	    printf("Marks     : %.2f\n", s1.marks);
	
	    return 0;
	}


## OUTPUT
Enter student name: John Doe
Enter roll number: 101
Enter marks: 88.5

Student Information:
Name      : John Doe
Roll No.  : 101
Marks     : 88.50


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	struct employee {
	    char name[50];
	    int id;
	    float basic_salary;
	    float hra;
	    float da;
	    float gross_salary;
	};
	
	int main() {
	    struct employee emp[3];
	    int i;
	
	    // Input details for 3 employees
	    for (i = 0; i < 3; i++) {
	        printf("Enter details for employee %d:\n", i + 1);
	        
	        printf("Name: ");
	        scanf(" %[^\n]", emp[i].name);  // read string with spaces
	        
	        printf("ID: ");
	        scanf("%d", &emp[i].id);
	        
	        printf("Basic Salary: ");
	        scanf("%f", &emp[i].basic_salary);
	        
	        printf("HRA: ");
	        scanf("%f", &emp[i].hra);
	        
	        printf("DA: ");
	        scanf("%f", &emp[i].da);
	
	        // Calculate gross salary
	        emp[i].gross_salary = emp[i].basic_salary + emp[i].hra + emp[i].da;
	        printf("\n");
	    }
	
	    // Display details
	    printf("Employee Details with Gross Salary:\n");
	    printf("--------------------------------------------------------\n");
	    printf("%-15s %-5s %-12s %-8s %-8s %-12s\n", "Name", "ID", "Basic Salary", "HRA", "DA", "Gross Salary");
	    printf("--------------------------------------------------------\n");
	
	    for (i = 0; i < 3; i++) {
	        printf("%-15s %-5d %-12.2f %-8.2f %-8.2f %-12.2f\n",
	               emp[i].name, emp[i].id, emp[i].basic_salary, emp[i].hra, emp[i].da, emp[i].gross_salary);
	    }
	
	    return 0;
	}
	

 ## OUTPUT
Enter details for employee 1:
Name: Alice Johnson
ID: 101
Basic Salary: 20000
HRA: 5000
DA: 3000

Enter details for employee 2:
Name: Bob Smith
ID: 102
Basic Salary: 25000
HRA: 6000
DA: 3500

Enter details for employee 3:
Name: Charlie Davis
ID: 103
Basic Salary: 18000
HRA: 4000
DA: 2500

Employee Details with Gross Salary:
--------------------------------------------------------
Name            ID    Basic Salary HRA      DA       Gross Salary
--------------------------------------------------------
Alice Johnson   101   20000.00     5000.00  3000.00  28000.00   
Bob Smith       102   25000.00     6000.00  3500.00  34500.00   
Charlie Davis   103   18000.00     4000.00  2500.00  24500.00   

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
	#include <stdio.h>
	
	struct student {
	    char name[10];     // Optional
	    int rollno;        // Optional
	    int subject[5];
	    int total;
	    float average;
	};
	
	int main() {
	    struct student s[2];
	    int i, j;
	
	    // Input marks for 2 students
	    for (i = 0; i < 2; i++) {
	        printf("Enter marks for student %d (5 subjects):\n", i + 1);
	        for (j = 0; j < 5; j++) {
	            printf("Subject %d: ", j + 1);
	            scanf("%d", &s[i].subject[j]);
	        }
	    }
	
	    // Calculate total and average for each student
	    for (i = 0; i < 2; i++) {
	        s[i].total = 0;
	        for (j = 0; j < 5; j++) {
	            s[i].total += s[i].subject[j];
	        }
	        s[i].average = s[i].total / 5.0f;
	    }
	
	    // Display results
	    printf("\nStudent-wise Total and Average Marks:\n");
	    for (i = 0; i < 2; i++) {
	        printf("Student %d: Total = %d, Average = %.2f\n", i + 1, s[i].total, s[i].average);
	    }
	
	    return 0;
	}


## OUTPUT
Enter marks for student 1 (5 subjects):
Subject 1: 75
Subject 2: 80
Subject 3: 78
Subject 4: 70
Subject 5: 71
Enter marks for student 2 (5 subjects):
Subject 1: 80
Subject 2: 85
Subject 3: 77
Subject 4: 72
Subject 5: 69

Student-wise Total and Average Marks:
Student 1: Total = 374, Average = 74.80
Student 2: Total = 383, Average = 76.60

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


