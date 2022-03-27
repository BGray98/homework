#include <stdio.h>

void print1 (int *ptr, int rows); //함수 print1 선언

int main()
{
    int one[] = {0, 1, 2, 3, 4}; //int형 배열 one 

    printf("one = %p\n", one); //one의 주소값
    printf("&one = %p\n", &one); //&one의 주소값;one의 주소값
    printf("&one[0] = %p\n", &one[0]); //&one[0]의 주소값;one의 주소값
    printf("\n");

    print1(&one[0], 5); //함수 print1 실행

    printf("[-----[조중훈] [2017038027]-----]");

    return 0;
}

void print1 (int *ptr, int rows) //함수 print1은 int형 포인터변수와 int형 변수를 받는다
{/* print out a one-dimensional array using a pointer */
    int i; //int형 변수 i
    
    printf ("Address \t Contents\n");
    
    for (i = 0; i < rows; i++) //row = 5
        printf("%p \t %5d\n", ptr + i, *(ptr + i)); //ptr+i의 주소는 one+i의 주소이고, ptr+i의 값은 one+i의 값이다
    printf("\n");
}
