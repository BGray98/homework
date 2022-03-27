#include <stdio.h>

#define MAX_SIZE 100 //MAX_SIZE의 정의;100

float sum(float [], int); //함수 sum 선언
float input[MAX_SIZE], answer; //MAX_SIZE만큼의 크기를 갖는 float형 전역배열 input과 float형 전역변수 answer
int i; //int형 전역변수 i 

int main(void)
{
    for(i=0; i < MAX_SIZE; i++) //배열 초기화;input[0]=0,input[1]=1,···,input[99]=99
        input[i] = i;
    /* for checking call by reference */
    printf("address of input = %p\n", input); //전역배열 input의 주소값
    
    answer = sum(input, MAX_SIZE); //변수 answer에 함수 sum이 반환한 값을 할당
    printf("The sum is: %f\n", answer); //answer의 변수값;input의 각 배열의 값의 총 합
    printf("[-----[조중훈] [2017038027]-----]");
    return 0;
}

float sum(float list[], int n) //함수 sum은 float형 배열과 int형 정수의 값을 받아 float 값을 반환한다
{
    printf("value of list = %p\n", list); //list의 값
    printf("address of list = %p\n\n", &list); //list의 주소

    int i; //int형 지역변수 i;전역변수 i와 무관
    float tempsum = 0; //float형 변수 tempsum
    
    for(i = 0; i < n; i++)
        tempsum += list[i]; //tempsum에 list의 각 배열의 값을 더함
    
    return tempsum; //tempsum 변수값 반환
}
