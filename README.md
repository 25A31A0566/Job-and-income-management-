# Job-and-income-management-
C language program
#include <stdio.h>
#include <string.h>

struct Job {
    int jobId;
    char jobName[50];
    char company[50];
    float monthlyIncome;
};

int main() {
    struct Job j[50];
    int choice, count = 0, i, searchId;
    float totalIncome = 0;

    do {
        printf("\n===== JOB & INCOME MANAGEMENT SYSTEM =====\n");
        printf("1. Add Job\n");
        printf("2. Display Jobs\n");
        printf("3. Search Job\n");
        printf("4. Calculate Total Income\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {

        case 1:
            printf("\nEnter Job ID: ");
            scanf("%d", &j[count].jobId);

            printf("Enter Job Name: ");
            scanf(" %[^\n]", j[count].jobName);

            printf("Enter Company Name: ");
            scanf(" %[^\n]", j[count].company);

            printf("Enter Monthly Income: ");
            scanf("%f", &j[count].monthlyIncome);

            count++;
            printf("Job added successfully!\n");
            break;

        case 2:
            if (count ==
