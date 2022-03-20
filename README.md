#include <stdio.h> //2017038027 소프트웨어학과 조중훈
int main()
{
int i; //int형 변수 선언
int *ptr;  //단일 포인터 변수 선언
int **dptr; //이중 포인터 변수 선언
i = 1234; //변수 i에 정수값 할당
printf("----조중훈 2017038027----");
printf("[checking values before ptr = &i] \n");
printf("value of i == %d\n", i); //i의 변수값
printf("address of i == %p\n", &i); //i의 주소값
printf("value of ptr == %p\n", ptr); //ptr의 변수값;쓰레기값
printf("address of ptr == %p\n", &ptr); //ptr의 주소값
ptr = &i; /* ptr is now holding the address of i */
printf("\n[checking values after ptr = &i] \n"); //포인터 변수 ptr에 i의 메모리 주소를 할당
printf("value of i == %d\n", i); //i의 변수값;변하지않음
printf("address of i == %p\n", &i); //i의 주소값;변하지않음
printf("value of ptr == %p\n", ptr); //ptr의 변수값;i의 주소값
printf("address of ptr == %p\n", &ptr); //ptr의 주소값;변하지 않음
printf("value of *ptr == %d\n", *ptr); //ptr 역참조값;i의 변수값과 동일
dptr = &ptr; /* dptr is now holding the address of ptr */
printf("\n[checking values after dptr = &ptr] \n"); //이중 포인터 변수 dptr에 ptr의 메모리 주소를 할당
printf("value of i == %d\n", i); //i의 변수값;변하지 않음
printf("address of i == %p\n", &i); //i의 주소값 변하지 않음
printf("value of ptr == %p\n", ptr); //ptr의 변수값;i의 주소값
printf("address of ptr == %p\n", &ptr); //ptr의 주소값;변하지않음
printf("value of *ptr == %d\n", *ptr); //ptr 역참조값;i의 변수값
printf("value of dptr == %p\n", dptr); //dptr의 변수값;ptr의 주소값
printf("address of dptr == %p\n", &dptr); //dptr의 주소값
printf("value of *dptr == %p\n", *dptr); //dptr의 역참조값;ptr의 변수값
printf("value of **dptr == %d\n", **dptr); //dptr의 이중 역참조값;i의 변수값
*ptr = 7777; /* changing the value of *ptr */
printf("\n[after *ptr = 7777] \n"); //포인터 변수 ptr의 역참조값에 정수값 대입
printf("value of i == %d\n", i); //i의 변수값;변함
printf("value of *ptr == %d\n", *ptr); //ptr의 역참조값
printf("value of **dptr == %d\n", **dptr); //dptr의 이중 역참조값;변함
**dptr = 8888; /* changing the value of **dptr */
printf("\n[after **dptr = 8888] \n"); //이중 포인터 변수 dptr의 이중 역참조값에 정수값 대입
printf("value of i == %d\n", i); //i의 변수값;변함
printf("value of *ptr == %d\n", *ptr); //ptr의 역참조값;변함
printf("value of **dptr == %d\n", **dptr); //dptr의 이중 역참조값
return 0;
}
