
#include <stdio.h>

int main() {
    char name[100];
    int marks[5];
    float average = 0;

    printf("Enter student name: ");
    fgets(name, sizeof(name), stdin);  // safer alternative to gets()

    printf("Enter marks for 5 subjects:\n");
    for(int i = 0; i < 5; i++) {
        printf("Subject %d: ", i+1);
        scanf("%d", &marks[i]);
        average += marks[i];
    }

    average /= 5;

    printf("\nStudent Name: %s", name);
    printf("Average Marks: %.2f\n", average);

    if(average >= 80) 
        printf("Grade: A+\n");
    else if(average >= 70) 
        printf("Grade: A\n");
    else if(average >= 60) 
        printf("Grade: A-\n");
    else if(average >= 50) 
        printf("Grade: B\n");
    else 
        printf("Grade: F\n");

    return 0;
}
