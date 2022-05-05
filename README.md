Q1) Program to understand nesting in the macros

// Online C compiler to run C program online
#include <stdio.h>
#define ISLOWER(c)  (c>=97 && c<=122)
#define ISUPPER(c)  (c>=65 && c<=90)
#define ISALPHA(c)  ISLOWER(c)  ||  ISUPPER(c)
#define ISNUM(c)  (c>=48 && c<=57)
#define ISALPHANUM(c)  ISALPHA(c) ||  ISNUM(c)
 main() {
     #define TOUPPER(c)  ((c) + 'A' - 'a')
     #define ISLEAP(y)  ((y%400 == 0)) || (y%100!=0 && y%4 ==0))
     #define BLANK_LINES(n) { int i; for(i=0;i<n;i++) printf("\n"); }
     #define CIRCLE_AREA(rad)  (3.14 * (rad) * (rad))
        
}

Q2) program to understand nesting in macros

#include <stdio.h>
#define ISLOWER(c)  (c>=97 && c<=122)
#define ISUPPER(c)  (c>=65 && c<=90)
#define ISALPHA(c)  ISLOWER(c)  ||  ISUPPER(c)
#define ISNUM(c)  (c>=48 && c<=57)
#define ISALPHANUM(c)  ISALPHA(c) ||  ISNUM(c)
 main() {
     char ch;
     printf("Enter a character : \n");
     scanf("%c",&ch);
     if(ISALPHANUM(ch))
         printf("%c is an alphanumeric : \n",ch);
     else
         printf("%c is not an alphanumeric character\n",ch);
    
}

Q3)

#include<stdio.h>
#define PROD(x,y)  ((x)*(y))
main()
{
    printf("%d\t",PROD(2,4));
    printf("%d\t",PROD(3+4,5+1));
    printf("%d\n",60/PROD(2,3));
}

Q4)
#include<stdio.h>
#define SQUARE(x)  ((x)*(x))
main()
{
    int k=5,s;
    s=SQUARE(k++);
    printf("s = %d, k = %d\n",s,k);
}

Q4) Program to uderstand  generic function

#include<stdio.h>
#define MAX(FNAME,DTYPE)           \
    DTYPE FNAME(DTYPE X, DTYPE Y)        \
    {                               \
        return X>Y ? X:Y;          \
    }          
    MAX(max_int,int)
    MAX(max_float,float)
    MAX(max_double,double)
    main()
    {
        int p;
        float q;
        double r;
        p=max_int(3,9);
        q=max_float(7.4,5.7);
        r=max_double(12.34,13.54);
        printf("p = %d,q = %.2f,r = %.21f \n",p,q,r);
    }
    
    Q5) Program to understand the use of stringizing operator
    
    #include<stdio.h>
#define SHOW(var,format)  printf(#var " = %" #format "\n",var);
main()
{
    int x=9;float y=2.5;char z='$';
    SHOW(x,d);
    SHOW(y,0.2f);
    SHOW(z,c);
    SHOW(x*y,0.2f);
}

Q6) program to understand the use of #if directives

#include<stdio.h>
#define FLAG 8
main()
{
    int a=20,b=4;
    #if FLAG >= 3
    printf("value of flag is greater than or equal to 3\n");
    a=a+b;
    b=a*b;
    printf("value of variable a and b have been changed\n");
    #endif
    printf("a= %d, b=%d\n",a,b);
    printf("program completed\n");
    
    
    
   
}
