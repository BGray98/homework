#include <stdio.h>
#include <stdlib.h>

int main()
{
    int list[5]; //int형 배열 
    int *plist[5] = {NULL,}; //int형 포인터 배열

    plist[0] = (int *)malloc(sizeof(int)); //포인터 배열 동적 할당;int형의 크기만큼
    
    list[0] = 1; //list[0]에 정수값 할당
    list[1] = 100; //list[1]에 정수값 할당
    
    *plist[0] = 200; //plist[0]가 가리키는 값에 정수값 할당

    printf("value of list[0] = %d\n", list[0]); //list[0]의 변수값;1
    printf("address of list[0] = %p\n", &list[0]); //list[0]의 주소값;list의 시작 주소값
    printf("value of list = %p\n", list); //list의 변수값;배열이므로 list의 시작 주소값
    printf("address of list (&list) = %p\n", &list); //&list의 주소값;list의 시작 주소값
    
    printf("----------------------------------------\n\n");
    printf("value of list[1] = %d\n", list[1]); //list[1]의 변수값;100
    printf("address of list[1] = %p\n", &list[1]); //list[1]의 주소값;list[0]의 주소값 + int형 변수의 크기(=4바이트)
    printf("value of *(list+1) = %d\n", *(list + 1)); //*(list의 주소값 + 배열의 크기(=4바이트)) -> *(list[1]의 주소값);list[1]의 변수값
    printf("address of list+1 = %p\n", list+1); //list의 주소값 + 배열의 크기(=4바이트) -> list[1]의 주소값;
    
    printf("----------------------------------------\n\n");
    printf("value of *plist[0] = %d\n", *plist[0]); //plist[0]가 가리키는 값의 변수값;200
    printf("&plist[0] = %p\n", &plist[0]); //plist[0]의 주소값;plist의 주소값
    printf("&plist = %p\n", &plist); //plist의 주소값
    printf("plist = %p\n", plist); //plist의 변수값; 배열이므로 plist의 시작 주소값
    printf("plist[0] = %p\n", plist[0]); //plist[0]의 변수값;동적할당 되었으므로 쓰레기값을 가짐
    printf("plist[1] = %p\n", plist[1]); //plist[1]의 변수값;동적할당 되지 않았으므로 값을 가지지 않는다
    printf("plist[2] = %p\n", plist[2]); // ""
    printf("plist[3] = %p\n", plist[3]); // ""
    printf("plist[4] = %p\n", plist[4]); //이하동문
    
    free(plist[0]); //동적 할당 해제
  
    printf("[-----[조중훈] [2017038027]-----]");

    return 0;
}
