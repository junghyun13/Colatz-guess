# Colatz-guess
# c program
# If the number entered is even, divide by 2, if the number entered is odd, multiply by 3, add 1, and return the number of times the same operation is repeated until the number is 1. However, if the given number is 1, it returns 0, and if it does not become 1 until the operation is repeated 500 times, it returns -1! 입력된 수가 짝수라면 2로 나누고 입력된 수가 홀수라면 3을 곱하고 1을 더하고 결과로 나온 수에 같은 작업을 1이 될 때까지 반복하는 횟수를 반환해보자! 단, 주어진 수가 1인 경우에는 0을, 작업을 500번 반복할 때까지 1이 되지 않는다면 –1을 반환한다!
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

int solution(int num) {
    int i;
    long long a=num;
    for(i=0;i<500;i++){
        if(a==1){
            return i;
        }
        else if(a%2==0){
            a/=2;
        }
        else{
            a=a*3+1;
        }
    }
    return -1;
}
int main(void){
   solution(6);
    return 0; }
#result--> 8 (6 → 3 → 10 → 5 → 16 → 8 → 4 → 2 → 1)
# pyhthon
def solution(num):
    cnt=0
    while(cnt<=500):
        if(num==1):
            return cnt
            break
        elif(num%2==0):
            num/=2
            cnt+=1
        elif(num%2==1):
            num=num*3+1
            cnt+=1
    return -1
a=solution(6)
print(a)
#result--> 8 (6 → 3 → 10 → 5 → 16 → 8 → 4 → 2 → 1)
