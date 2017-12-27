# finally-test
point and linked list
#include "stdafx.h"
#include<iostream>
using namespace std;
struct student
{
 char name[50];
 char num[20];
 int age;
 struct student *next;
};
int main()
{
 struct student *p,*q,*head;
 int s;
 head=new student;
 q=head;
 p=q;
 cout<<"输入学生信息:"<<endl;
 cin>>p->name;
 cout<<"输入学生学号:"<<endl;
 cin>>p->num;
 cout<<"输入学生年龄:"<<endl;
 cin>>p->age;
 while(cout<<"1or2?"<<endl<<"1 go on"<<endl<<"2 stop"<<endl,cin>>s,s==1)
 {
  p=new student;
  q->next=p;
  q=p;
  cin>>p->name;
  cin>>p->num;
  cin>>p->age;
  p->next=NULL;
 }
 p=head;
 while(p!=NULL)
 
 {
   cout<<"姓名"<<p->name<<endl<<"学号"<<p->num<<endl<<"年龄"<<p->age<<endl;
  p=p->next;
 }
  p=head;
 do
 {
  q=p->next;
  delete p;
  p=q;
 }while(q);
}
