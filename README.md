# Programowanie-obiektowe

//7.2.1
#include <stdio.h>

struct trojkat{
    int a;
    int b;
    int c;
};

int f(struct trojkat jeden)
{
    return jeden.a+jeden.b+jeden.c;
}


//7.2.2
#include <stdio.h>

struct trojkat{
    int a;
    int b;
    int c;
};

void f(struct trojkat troj1, struct* trojkat troj2)
{
    troj2.a=troj1.a;
    troj2.b=troj1.b;
    troj2.c=troj1.c;
}


//7.2.3
#include <stdio.h>

struct punkt{
    float x;
    float y;
    float z;
};

void f(int n, float tab[n], struct punkt)
{
    float tab2[3];
    for(int i=0; i<n; i++)
    {
        float minx=999.0;
        float miny=999.0;
        float minz=999.0;
        float a,b,c;
        if(i%3=0 || i==0)
        {
            if(tab[i]<tab[i+3])
            {
            a=(tab[i]-tab[i+3])*(-1);
            if(a<minx)
                minx=a;
            }
            else
            {
            a=tab[i]-tab[i+3];
            if(a<minx)
                minx=a;
            }
        }
        if(i%3=1)
        {
            if(tab[i]<tab[i+3])
            {
            b=(tab[i]-tab[i+3])*(-1);
            if(b<minx)
                miny=b;
            }
            else
            {
            b=tab[i]-tab[i+3];
            if(b<minx)
                miny=b;
            }
        }
        if(i%3=2)
        {
            if(tab[i]<tab[i+3])
            {
            c=(tab[i]-tab[i+3])*(-1);
            if(c<minx)
                minz=c;
            }
            else
            {
            c=tab[i]-tab[i+3];
            if(c<minx)
                minz=c;
            }
        }
    }
    tab2[0]=minx;
    tab2[1]=miny;
    tab2[2]=minz;
    for(int i=0; i<3; i++)
    {
        printf("%f", tab2[i]);
    }
    
}
