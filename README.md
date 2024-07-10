# n-student
#include<stdio.h>
#include<conio.h>
struct student
{
    char studname[25],stream[5];
    int rollno,m1,m2,m3,m4,total;
    float avg;
};
void main()
{
    int n,i;
    printf("\n ENTER NUMBER OF STUDENT:");
    scanf("%d",&n);
    struct student stud[n];
    printf("\n ENTER STUDENT DETAILS:-");
    for(i=0;i<n;i++)
    {
        printf("\n ENTER STUDENT NAME:");
        scanf("%s",&stud[i].studname);
        printf("\n ENTER STREAM:");
        scanf("%s",&stud[i].stream);
        printf("\n ENTER ROLLNO:");
        scanf("%d",&stud[i].rollno);
        printf("\n ENTER MARKS IN 4 SUBJECTS:");
        scanf("%d %d %d %d",&stud[i].m1,&stud[i].m2,&stud[i].m3,&stud[i].m4);
        stud[i].total=stud[i].m1+stud[i].m2+stud[i].m3+stud[i].m4;
        stud[i].avg=stud[i].total/4;
    }
    printf("\n STUDENTNAME  ROLLNO  STREAM  SUB1  SUB2  SUB3  SUB4  TOTAL  AVG  \n");
    for(i=0;i<n;i++)
    {
        printf("\n%s\t%d\t%s\t%d\t%d\t%d\t%d\t%d\t%.2f",stud[i].studname,stud[i].rollno,stud[i].stream,stud[i].m1,stud[i].m2,stud[i].m3,stud[i].m4,stud[i].total,stud[i].avg);
    }
    getch();
}

