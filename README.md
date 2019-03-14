
#include <stdio.h>
void main()
{
    int a[100];
    int i,j,a=0,s=0,b=0;// a为最后要输出的重数  s为记录第几个数为重数
    int n;                                           //b为当前的数的个数
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);       //从键盘输入数组
    }
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)   //遍历数组
        {
            if(a[j]==a[i])
                b++;
        }
        if(b>a)  //将其数量和之前的数量相比，大的话就交换，小的话就不变
        {
            a=b;
            s=i;        //记录当前重数在数组中的位置
        }
        b=0;      //初始化
    }
    printf("众数是：%d\n重数是：%d\n",a[s],a);
}
