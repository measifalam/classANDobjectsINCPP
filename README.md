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
