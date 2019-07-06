#include <stdio.h>
#include <stdlib.h>
int wish,total,a,b,c;
int ordrspy1=0;
int Qnty1=0;
int ordrspy2=0;
int Qnty2=0;
int ordrspy3=0;
int Qnty3=0;
int rspy()
{
     printf("  our recipes...\n");
     printf("  1.Grilled chicken          ---$120\n");
     printf("  2.Fried chicken bolls      ---&170\n");
     printf("  3.Tandoori chicken chips   ---$150\n");
     printf("  we are awaiting for your order......\n");
     printf("  Do you want to taste our recipes ? if yes press 1,if No press 0 \n");
     scanf("%d",&a);
     if(a==1)
     {

             printf("enter the order number and quantity");
         scanf("%d\t%d",&ordrspy1,&Qnty1);
         printf("you order was taken...\ndo you want order anything else? if yes press 1,if No press 0\n");
         scanf("%d",&b);
         if(b==1)
         {
           printf("enter the order number and quantity");
             scanf("%d\t%d",&ordrspy2,&Qnty2);
             printf("you order was taken...\ndo you want order anything else? if yes press 1,if No press 0\n");
             scanf("%d",&c);
             if(c==1)
             {
                 printf("enter the order number and quantity");
                 scanf("%d\t%d",&ordrspy3,&Qnty3);
                 printf("you order was taken...\n");
             }
         }
         else
            printf(" thanks for your order..The recipes touch your door within one hour...\n");
           wrk();
     }
     else
     return wrk() ;
     orderedrecipes(ordrspy1,Qnty1);
     orderedrecipes(ordrspy2,Qnty2);
     orderedrecipes(ordrspy3,Qnty3);
}
int orderedrecipes()
{
    printf("    payment details...\n  your ordered list");
    printf("\nS.no    Recipe        Quantity      Amount\n");
    printf("1.");
    if(ordrspy1==1)
    {
        printf("Grilled chicken          %d       $%d\n",Qnty1,120*Qnty1);
    }
     if(ordrspy1==2)
    {
        printf("Fried chicken bolls      %d       $%d\n",Qnty2,170*Qnty2);
    }
     if(ordrspy1==3)
    {
        printf("Tandoori chicken chips   %d       $%d\n",Qnty3,150*Qnty3);
    }
    total=((120*Qnty1)+(170*Qnty2)+(150*Qnty3));

    printf("        \t    total    $%d",total);
    return wrk();
}
int wrk()
{
    printf("\n WELCOME TO eatme.com\n");
    printf(" create your tasty and crispy day in your life with eatme.com\n");
    printf("  1.View our recipes\n");
    printf("  2.view your ordered recipes\n");
    printf("  3.Billing \n");
    printf("  4.please touch us with your delicious feedback..\n ");
    printf(" 5.exit()\n");
    printf(" enter you wish!!\t");
    scanf("%d",&wish);
    switch(wish)
    {
    case 1:
        rspy();
        break;
    case 2:
        orderedrecipes();
        break;
    case 3:
        break;
    case 4:
        break;
    case 5:
        printf("thanks for visiting us..");
        return ;
        break;
    default:
        printf("pls enter the valid wish");
        break;
    }

}
int main()
{
    printf("eatme.com");
    wrk();
    return 0;
}
