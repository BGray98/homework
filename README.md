#include <stdio.h>

struct student1 { //구조체 student1
    char lastName;
    int studentId;
    char grade;
};

typedef struct { //typedef 구조체 student2
    char lastName;
    int studentId;
    char grade;
} student2;

int main() {
    struct student1 st1 = {'A', 100, 'A'}; //구조체 student1 st1 초기화

    printf("st1.lastName = %c\n", st1.lastName);
    printf("st1.studentId = %d\n", st1.studentId);
    printf("st1.grade = %c\n", st1.grade);

    student2 st2 = {'B', 200, 'B'}; //구조체 student2 st2 초기화

    printf("\nst2.lastName = %c\n", st2.lastName);
    printf("st2.studentId = %d\n", st2.studentId);
    printf("st2.grade = %c\n", st2.grade);

    student2 st3; //구조체 student2 st3 선언

    st3 = st2; //st3에 st2 복사

    printf("\nst3.lastName = %c\n", st3.lastName);
    printf("st3.studentId = %d\n", st3.studentId);
    printf("st3.grade = %c\n", st3.grade); //복사됨
    /* equality test */

    if(st3 == st2) /* not working */ //전체 구조의 동등성 검사 오류발생; 구조 치환 하여 각각의 구조체의 값의 동등성 검사 실행 필요
        printf("equal\n");
    else
        printf("not equal\n"); 

    printf("[-----[조중훈] [2017038027]-----]");

    return 0;
}
