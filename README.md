#include <stdio.h>
#include <stdlib.h>

int main()
{
    int list[5]; //int형 배열 list
    int *plist[5]; //int형 포인터 배열 plist

    list[0] = 10; //list[0]에 변수값 대입
    list[1] = 11; //list[1]에 변수값 대입

    plist[0] = (int*)malloc(sizeof(int)); //plist 동적 할당

    printf("list[0] \t= %d\n", list[0]); //list[0]의 변수값
    printf("address of list \t= %p\n", list); //list의 주소값
    printf("address of list[0] \t= %p\n", &list[0]); //list[0]의 주소값;list의 주소값과 동일
    printf("address of list + 0 \t= %p\n", list+0); //list + 0 의 주소값;list[0]의 주소값
    printf("address of list + 1 \t= %p\n", list+1); //list + 1 의 주소값;4바이트 증가하여 list[1]의 주소값
    printf("address of list + 2 \t= %p\n", list+2); //list + 2 의 주소값;8바이트 증가하여 list[2]의 주소값
    printf("address of list + 3 \t= %p\n", list+3); //list + 3 의 주소값;12바이트 증가하여 list[3]의 주소값
    printf("address of list + 4 \t= %p\n", list+4); //list + 4 의 주소값;16바이트 증가하여 list[4]의 주소값
    printf("address of list[4] \t= %p\n", &list[4]); //list[4]의 주소값

    free(plist[0]); //동적 할당 해제

    printf("[-----[조중훈] [2017038027]-----]");

    return 0;
}
