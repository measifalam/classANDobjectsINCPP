# classANDobjectsINCPP
C++ Classes and Objects. Class: A class in C++ is the building block, that leads to Object-Oriented programming. It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A C++ class is like a blueprint for an object.
//1.Access Data memeber through structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;
  
struct item
{
 int codeno;
 int prize;
 int qty;
};

int main()
{
 struct item a, * b;
 a.codeno=123;
 a.prize=150;
 a.qty=150;
 printf("With Simple Variable");
 printf("\n Code No.=%d",a.codeno);
 printf("\n Prize=%d",a.prize);
 printf("\n Quantity=%d",a.qty);
 
 b->codeno=124;
 b->qty=75;
 b->prize=200;
 
 printf("With Pointer Variable");
 printf("\n Code No.=%d",b->codeno);
 printf("\n Prize=%d",b->prize);
 printf("\n Quantity=%d",b->qty);
 
 return 0;
}

=========================

//3.Implementation of class in c++
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class item
{
public:
       int codeno;
       int prize;
       int qty;
};

int main()
{
item one;
one.codeno=123;
one.prize=123.45;
one.qty=150;

cout<<"\n Code No="<<one.codeno<<endl;
cout<<"\n Prize="<<one.prize<<endl;
cout<<"\n Quantity="<<one.qty<<endl;
return 0;
}

==================

//4.using class to declare member variable & func under protected section
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class A
{
 protected:
      int num;
      void display()
       {
         cout<<num;
       }
};
int main()
{
  A a;
  a.num=100;
  a.display();
  return 0;
}

//Above program gives an error A::num and A::display() because not accessible

=========================

//5.class to declare member variable and function private,public, and protected section 
~~~~~~~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class sample
{
  private: 
         int num;
         void show1()
         {
           cout<<"Inside private section"<<endl;
           cout<<"Enter a number"<<endl;
           cin>>num;
           cout<<"Number is:"<<num;
          }
          
 public:
        int num1;
        void show()
        {
          show1();
          cout<<"\n\n Inside the public section:";
          cout<<"\n Enter a number:";
          cin>>num1;
          cout<<"Number is:"<<num1;
          show2();
        }
        
  protected:
        int num2;
        void show2()
        {
        cout<<"\n \n Inside the protected section";
        cout<<"\n Enter a number:";
        cin>>num2;
        cout<<"Number is:"<<num2;
        }
};

int main()
{
  sample s;
  s.show();
  return 0;
}

================

//6.To access private members of a class using member function
~~~~~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class item
{
  private:
     int codeno;
     float price;
     int qty;
     
  public:
     void show()
     {
      codeno=125;
      price=195;
      qty=200;
      cout<<"\n Codeno.="<<codeno;
      cout<<"\n Price="<<price;
      cout<<"\n Quantity="<<qty;
     }
};

int main()
{
 item one;
 one.show();
 return 0;
}

=============

//7.Program o declare private member function and access it using public member function
~~~~~~~~~~~~~~~
#include<iostream>
using namespace std;

struct item
{
 private:
    int codeno;
    float price;
    int qty;
    
    void values()
    {
      codeno=125;
      price=195;
      qty=200;
    }
    
  public:
      void show()
      {
        values();
        cout<<"\n Codeno="<<codeno;
        cout<<"\n Price="<<price;
        cout<<"\n Quantity="<<qty;
      }
 };

int main()
{
  item one;
  one.show();
  return 0;
}

===========

//8.To define member function of class outside the class
~~~~~~~~~~~~~~~

#include<iostream>

class item
{
  private:
       int codeno;
       float price;
       int qty;
       
  public:
       void show(void);
};

void item::show()
{
  codeno=101;
  price=2342;
  qty=122;
  cout<<"\n Codeno="<<codeno;
  cout<<"\n Price="<<price;
  cout<<"\n Quantity="<<qty;
}

int main()
{
item one;
one.show();
return 0;
}

========

//9.Program to make an outside function as inline
~~~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class item
{
  private:
     int codeno;
     float price;
     int qty;
     
  public:
     void show(void);
};

inline void item::show()
{
  codeno=213;
  price=2022;
  qty=150;
  cout<<"\n Codeno="<<codeno;
  cout<<"\n Price="<<price;
  cout<<"\n Quantity="<<qty;
}

int main()
{
  item one; 
  one.show();
  return 0;
}

========

//10. To calculate Simple Interest
~~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class interest
{
  private:
    float p_amount;
    float rate;
    float period;
    float interest;
    float t_amount;
  
  public:
    void in()
    {
      cout<<"Principle Amount:";
      cin>>p_amount;
      
      cout<<"Rate of Interest:";
      cin>>rate;
      
      cout<<"Numbers of years:";
      cin>>period;
      
      interest=(p_amount*period*rate)/100;
      t_amount=interest + p_amount;
    }
    
    void show()
    {
       cout<<"Principle Amount:"<<p_amount;
       cout<<"Rate of Interest:"<<rate;
       cout<<"Numbers of years:"<<period;
       cout<<"Interest:"<<interest;
       cout<<"Total Amount:"<<t_amount;
    }   
};

int main()
{
  interest r;
  r.in();
  r.show();
  return 0;
}

==========

//11.To declare class with private,public and private sections.Declare object & access data element

#include<iostream>
using namespace std;

class access
{
  private:
    int p;
    void getp()
    {
      cout<<"\n In pget() enter value of p:";
      cin>>p;
    }
    
    public:
    int h;
    void geth()
    {
      cout<<"\n In geth() :"<<endl;
      getp();
      getm();
      cout<<"p="<<p<<"h="<<h<<"m="<<m;
    }
    protected:
       int m;
       void getm()
       {
        cout<<"In mget() enter value of m:";
        cin>>m;
       }
};

int main()
{
  access a;
  a.h=4;
  a.geth();
  return 0;
}

=========

#include<iostream>
using namespace std;

class month
{
 public:
     char *name;
     int days;
};

int main()
{
  month M1,M3;
  M1.name="January";
  M1.days=31;
  M3.name="March";
  M3.days=31;
  cout<<"\n Object M1";
  cout<<"\n Month name:"<<M1.name<<"Address:"<<(unsigned)&M1.name;
  cout<<"\n Days:"<<M1.days<<"\t \t Address:"<<(unsigned)&M1.days;
  cout<<"\n \n Objects M3";
  cout<<"\n Month Name:"<<M3.name<<"\t Address:"<<(unsigned)&M3.name;
  cout<<"\n Days:"<<M3.days<<"M3.days<<"\t\t Address:"<<(unsigned)&M3.days;
  return 0;
 }
 
 ==========
 
 //13.To display the size of the objects
 ~~~~~~~~~~~
 
 #include<iostream>
 using namespace std;
 
 class data
 {
   long i;
   float f;
   char c;
 };
 
 int main()
 {
   data d1,d2;
   cout<<endl<<"Size of object d1="<<sizeof(d1);
   cout<<endl<<"Size of object d2="<<sizeof(d2);
   cout<<endl<<"Size of class="<<sizeof(data);
   return 0;
 }
 
 ==========
 
//14.To declare static data member
~~~~~~~~`

#include<iostream>
using namespace std;

class number
{
  static int c;
  
  public:
     void count()
     {
       ++c;
       cout<<"\n C="<<c;
     }
};

int number::c=0;
int main()
{
  number a,b,c;
  a.count();
  b.count();
  c.count();
  return 0;
}

=====

//15.To show the diffirence between static & non-static member variable
~~~~~~~~~~~~~~

#include<iostream>
using namespace std;

class number
{
 static int c;
 int k;
 public:
    void zero()
    {
      k=0;
    }
    void count()
    {
      ++c;
      ++k;
      cout<<"\n Value of C="<<c<<"Address of C="<<(unsigned)&c;
      cout<<"\n Value of k="<<k<<"Address of K="<<(unsigned)&k;
    }
};
 
int number::c=0;
int main()
{
  number A,B,C;
  A.zero();
  B.zero();
  C.zero();
  A.count();
  B.count();
  C.count();
  return 0;
}
