# Inheritance-in-C-
#include<iostream.h>
#include<conio.h>
class Base
{
public:
    int a,b;
    void get();
};

class Derived:public Base
{
public:
    int c;
    void mul();
};

class Derived1:public Derived
{
public:
    int d;
    void product();
};

class Base2
{
public:
    void show();
};

class Derived2:public Derived1,public Base2
{
public:
    int e;
    void multiply();
};

class Derived3:public Base
{
public:
    int c;
    void show();
};

void Base::get()
{
    cout<<"\nEnter 2 values : ";
    cin>>a>>b;
}

void Derived:: mul()
{
    c=a*b;
    cout<<"\nResult is : "<<c;
}

void Derived1::product()
{
    cout<<"\n\n Enter 2 values: ";
    cin>>b>>c;
    d=b*c;
    cout<<"\nResult is : "<<d;
}

void Derived2::multiply()
{
    cout<<"\n\n Enter 2 values : ";
    cin>>c>>d;
    e=c*d;
    cout<<"\nResult is : "<<e;
}

void Derived3::show()
{
    cout<<"\n\nEnter 2 values : ";
    cin>>a>>b;
    c=a*b;
    cout<<"\nResult is : "<<c;
}

int main()
{
    //clrscr();
    cout<<"\n\n\t IMPLEMENTATION OF HYBRID INHERITANCE ";
    cout<<"\n\n\n\n";
    cout<<"\n\t **** SINGLE INHERITANCE ***\n";
    Derived2 d;
    d.get();
    d.mul();
    cout<<"\n\n\t **** MULTILEVEL INHERITANCE ****\n";
    d.product();
    cout<<"\n\n\t **** MULTIPLE INHERITANCE ****\n";
    d.multiply();
    Derived3 d1;
    cout<<"\n\n\t **** HIERARCHICAL INHERITANCE ****";
    d1.show();
    getch();
    return 0;
}
