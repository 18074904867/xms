
#include <stdio.h>
void main()
{
    int a[100];
    int i,j,maxcount=0,index=0,ncount=0;// maxcount为最后要输出的重数  index为记录第几个数为重数
    int n;                                           //ncount为当前的数的个数
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
                ncount++;
        }
        if(ncount>maxcount)  //将其数量和之前的数量相比，大的话就交换，小的话就不变
        {
            maxcount=ncount;
            index=i;        //记录当前重数在数组中的位置
        }
        ncount=0;      //每次注意初始化，不然就会gg哦
    }
    printf("众数是：%d\n重数是：%d\n",a[index],maxcount);
}
