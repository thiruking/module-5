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
```
#include <stdio.h>

int main() {
    float length, width, area;
    float *ptr_length, *ptr_width;


    ptr_length = &length;
    ptr_width = &width;

   
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptr_length);

    printf("Enter the width of the rectangle: ");
    scanf("%f", ptr_width);


    area = (*ptr_length) * (*ptr_width);

   
    printf("The area of the rectangle is: %.2f\n", area);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/3cb21060-0812-4e93-ae3b-8129c46210e6)
		       	


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
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str;

    str = (char *)malloc(8 * sizeof(char));

   
    if (str == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }

    
    strcpy(str, "WELCOME");

  
    printf("%s\n", str);

 
    free(str);

    return 0;
}


```

## OUTPUT

![image](https://github.com/user-attachments/assets/096fb5f6-fe49-4f79-84e5-92e0ce55f5d3)


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
```
#include <stdio.h>

struct student {
    char name[50];
    int roll_number;
    float marks;
};

int main() {
    struct student s;

  
    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.roll_number);
    printf("Enter marks: ");
    scanf("%f", &s.marks);

  
    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_number);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/c57ea73e-aaed-408b-ab38-1f08d0f0e02c)


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
```
#include <stdio.h>


struct Employee {
    int id;
    char name[50];
    float basic_salary;
    float hra;
    float da;
    float gross_salary;
};

int main() {
    struct Employee emp[3]; 
    int i;

   
    for (i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Name: ");
        scanf("%s", emp[i].name);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);
        printf("HRA: ");
        scanf("%f", &emp[i].hra);
        printf("DA: ");
        scanf("%f", &emp[i].da);

        
        emp[i].gross_salary = emp[i].basic_salary + emp[i].hra + emp[i].da;
    }

  
    printf("\n--- Employee Details and Gross Salary ---\n");
    for (i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("ID: %d\n", emp[i].id);
        printf("Name: %s\n", emp[i].name);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("HRA: %.2f\n", emp[i].hra);
        printf("DA: %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

    return 0;
}

```


 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/ac66fc0e-9e10-48c9-b635-913912cd5ea8)
 ![image](https://github.com/user-attachments/assets/0b60ec63-1a8c-40d7-9743-ba0fbbbfcfa2)



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
```
#include <stdio.h>


struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];  
    int i, j;
    float average;

    for (i = 0; i < 2; i++) {
        printf("\nEnter details for Student %d:\n", i + 1);
        printf("Enter Name: ");
        scanf("%s", s[i].name);
        printf("Enter Roll Number: ");
        scanf("%d", &s[i].rollno);

        printf("Enter marks for 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
        }
    }

   
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    printf("\n--- Student Marks Report ---\n");
    for (i = 0; i < 2; i++) {
        average = s[i].total / 5.0;
        printf("\nStudent %d:\n", i + 1);
        printf("Name: %s\n", s[i].name);
        printf("Roll No: %d\n", s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", average);
    }

   
    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/71a64c6e-b37e-4d23-99c0-05161af7207b)

![image](https://github.com/user-attachments/assets/72a24c9d-ebec-4914-ac56-6f8ea4d20c9f)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


