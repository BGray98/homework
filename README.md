#include<stdio.h>
#include<stdlib.h>

int main()
{
    int **x; //int형 이중 포인터 변수 x 

    printf("sizeof(x) = %lu\n", sizeof(x)); //x의 크기 4 * 1 * 1 = 4
    printf("sizeof(*x) = %lu\n", sizeof(*x)); //*x의 크기 4 * 1 = 4
    printf("sizeof(**x) = %lu\n", sizeof(**x)); //**x의 크기 4

    printf("[-----[조중훈] [2017038027]-----]");
    
    return 0;
}
