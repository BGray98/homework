#include <stdio.h> //2017038027 소프트웨어학과 조중훈 hw2-1

int main()
{
char charType; //char형 변수 선언
int integerType; //int형 변수 선언
float floatType; //float형 변수 선언
double doubleType; //double형 변수 선언
printf("----조중훈 2017038027----");
printf("Size of char: %ld byte\n",sizeof(charType)); //char형 변수의 크기는 1byte
printf("Size of int: %ld bytes\n",sizeof(integerType)); //int형 변수의 크기는 4byte
printf("Size of float: %ld bytes\n",sizeof(floatType)); //float형 변수의 크기는 4byte
printf("Size of double: %ld bytes\n",sizeof(doubleType)); //double형 변수의 크기는 8byte
printf("-----------------------------------------\n");
printf("Size of char: %ld byte\n",sizeof(char)); //char형 자료형의 크기는 1byte
printf("Size of int: %ld bytes\n",sizeof(int)); //int형 자료형의 크기는 4byte
printf("Size of float: %ld bytes\n",sizeof(float)); //float형 자료형의 크기는 4byte
printf("Size of double: %ld bytes\n",sizeof(double)); //double형 자료형의 크기는 8byte
printf("-----------------------------------------\n");
printf("Size of char*: %ld byte\n",sizeof(char*));
printf("Size of int*: %ld bytes\n",sizeof(int*));
printf("Size of float*: %ld bytes\n",sizeof(float*));
printf("Size of double*: %ld bytes\n",sizeof(double*)); //포인터 변수는 자료형과 관계 없이 항상 4byte (32비트 기준)
return 0;
}
