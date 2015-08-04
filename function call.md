# zy_8_4
//
//  main.m
//  Lesson_8_4
//
//  Created by lanou3g on 15/8/3.
//  Copyright (c) 2015年 lanou3g. All rights reserved.
//

#import <Foundation/Foundation.h>
#pragma mark 加和
void sum(int n)
{
    int sum = 0;
    for (int i = 0; i <= n; i ++) {
        sum += i;
    }

    printf("%d\n",sum);
}
#pragma mark 哪一天
void dayOfYear(year, month,day)
{
    
    if (year % 400 == 0 ||(year % 4 ==0 && year % 100!= 0)) {
        int day1[12] = {0,31,60,91,121,152,182,213,244,274,305,335};
        switch (month) {
            case 1:
                printf("第%d天\n",day);
                break;
            case 2:
                printf("第%d天\n",day + day1[1]);
                break;
            case 3:
                printf("第%d天\n",day + day1[2]);
                break;
            case 4:
                printf("第%d天\n",day + day1[3]);
                break;
            case 5:
                printf("第%d天\n",day + day1[4]);
                break;
            case 6:
                printf("第%d天\n",day + day1[5]);
                break;
            case 7:
                printf("第%d天\n",day + day1[6]);
                break;
            case 8:
                printf("第%d天\n",day + day1[7]);
                break;
            case 9:
                printf("第%d天\n",day + day1[8]);
                break;
            case 10:
                printf("第%d天\n",day + day1[9]);
                break;
            case 11:
                printf("第%d天\n",day + day1[10]);
                break;
            case 12:
                printf("第%d天\n",day + day1[11]);
                break;
            
        }
        
    }else{
        int day1[12] = {0,31,59,90,120,151,181,212,243,273,304,334};
        switch (month) {
            case 1:
                printf("第%d天\n",day);
                break;
            case 2:
                printf("第%d天\n",day + day1[1]);
                break;
            case 3:
                printf("第%d天\n",day + day1[2]);
                break;
            case 4:
                printf("第%d天\n",day + day1[3]);
                break;
            case 5:
                printf("第%d天\n",day + day1[4]);
                break;
            case 6:
                printf("第%d天\n",day + day1[5]);
                break;
            case 7:
                printf("第%d天\n",day + day1[6]);
                break;
            case 8:
                printf("第%d天\n",day + day1[7]);
                break;
            case 9:
                printf("第%d天\n",day + day1[8]);
                break;
            case 10:
                printf("第%d天\n",day + day1[9]);
                break;
            case 11:
                printf("第%d天\n",day + day1[10]);
                break;
            case 12:
                printf("第%d天\n",day + day1[11]);
                break;
                
        }
    }
    

}

#pragma mark 中间值
void mid(int num1,int num2,int num3)
{
     int max = num1 > num2 ? num1 :num2;
     int max1 = max > num3 ? max :num3;
     int min = num1 > num2 ? num2 : num1;
     int min1 = min > num3 ? num3 :min;
     int midnum = num1 + num2 + num3 - max1 -min1;
    
//    int  d = cc > dd ? dd: cc;
    int d ;
    if (num1 > num2 && num2 > num3) {
        d = num2;
    }
    if (num1 > num3 && num3 > num2) {
        d = num3;
    }
    if (num3 > num1 && num1 > num2) {
        d = num1;
    }
    printf("中间值是: %d %d\n",d,midnum);
}
#pragma mark 位数
void weiShu(int a)
{
    int count = 1;
    while ((a / 10) > 0)
    {
        a = a / 10;
        count ++;
    }

    printf("%d位\n",count);

}

#pragma mark 阶乘
int jieCheng(int n)
{
    
    if (n > 1) {
         n *= jieCheng(n - 1);
       
    }
    
    return n;
}
#pragma mark 累加
int leiJia(int n)
{
    if (n > 0) {
        n += leiJia(n -1);
    }
    return n;
}
#pragma mark 交换值
void changeValue(int num1,int num2)
{
    num1 = num1 ^ num2;
    num2 = num1 ^ num2;
    num1 = num1 ^ num2;
    printf("%d %d\n",num1,num2);


}
int main(int argc, const char * argv[]) {
//    1.无返回值.无参数
//    void test();
//    2.无返回值,有参数
//    void [test1(char a[ ]);
//    3.有返回值,无参数
//     void test2()
//    {
//        return 0;
//    }
//    4.有返回值,有参数
//     void test3(int a)
//    {
//        return a + 100;
//    }
//     return 的作用
//    1.结束当前函数的执行
//    2.返回一个结果
//    主调函数:主动调用其它函数的函数
//    被调函数:被调用的函数.
#pragma mark   形参:
//    形式参数,出现在函数定义中,储存提供给函数使用的值.
#pragma mark   实参:
//    实际参数,出现在函数的调用中,为函数的执行提供值.
//     实参 给形数 赋值 是拷贝实现的
    
    
    
    
    
    
    int a,b,c;
   // scanf("%d,%d,%d",&a,&b,&c);
        a = arc4random() % (30 - 10 + 1) + 10;
        b = arc4random() % (30 - 10 + 1) + 10;
        c = arc4random() % (30 - 10 + 1) + 10;
    printf("%d  %d  %d\n",a,b,c);
   mid(a, b, c);
//    int n;
//    scanf("%d",&n);
//    sum(n);
//    return 0;
//    int year,month,day;
//    scanf("%d%d%d",&year,&month,&day);
//    dayOfYear(year, month, day);
//    int a ;
//    scanf("%d",&a);
//    weiShu(a);
//    int n;
//    scanf("%d",&n);
//    
//    printf("%d\n",jieCheng(n));
//    int num1,num2;
//    scanf("%d%d",&num1,&num2);
//    changeValue(num1,num2);
//    int n ,sum;
//    scanf("%d",&n);
//    sum = leiJia(n);
//    printf("%d\n",sum);
    
}
