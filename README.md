#include <stdio.h>

struct student { //구조체 student
    char lastName[13]; /* 13 bytes */ //char형 크기 1byte * 배열의 길이 13  = 13byte
    int studentId; /* 4 bytes */ //int형 크기 4byte
    short grade; /* 2 bytes */ //short형 크기 2byte
};

int main()
{
    struct student pst; //구조체 student pst

    printf("size of student = %ld\n", sizeof(struct student));
    //구조체 student의 크기; 가장 큰 int형 크기 4byte 기준 13(+3) + 4 + 2(+2) = 24byte (괄호는 padding)
    printf("size of int = %ld\n", sizeof(int)); //int형의 크기;4byte
    printf("size of short = %ld\n", sizeof(short)); //short형의 크기;2byte

    printf("[-----[조중훈] [2017038027]-----]");

    return 0;
}
