# oop imbo-01-18 практика Лялина Екатерина

Сделать форк этого репозитория и загрузить к себе в репозиторий текст программы. 

Практическая работа 1. Вариант 1.

#include <iostream>
#include <string>
using namespace std;
int main()
{
  string name;
  cout << "What is your name? ";
  getline (cin, name);
  cout << "Hello, " << name << "!\n";
  return 0;
}


Практическая работа 2. Вариант 4.
#include <iostream>
#include <math.h>
using namespace std;
int main()
{
  setlocale(LC_ALL, "Russian");
  float x,a,y,t;
  cout << "Введите х: \n";
  cin >> x;
  cout << "Введите а: \n";
  cin >> a;
  if (x<a) y=sqrt(sin(a*x)); else y=a+log(x+a);
  if (y>a) t=tan(a*x)+cos(2*a*y);
  if (a=y) t=y/(a-x)+(a+x)/(y*y);
  if (a>y) t=y/(a-x);
  cout << "Значение t=" << t << "\n";
  cout << "Значение у=" << y << "\n";
  return 0;
}
  

Практическая работа 3. Вариант 7.

#include <iostream>
#include <locale>
using namespace std;

struct book {
string name;
string autor;
string genre;
int year;
int code;
};

int main()
{
    book a[10];
    int u;
    int i=0;
    int j;
    string p;
    setlocale(LC_ALL, "Russian");
    cout << "Добро пожаловать!\n";
    do {
    cout << "Меню:\n1. Чтобы внести данные о книге, введите 1.\n2. Чтобы получить данные о книге, введите 2.\n3. Чтобы выйти из программы, введите 3.\n";
    cin >> u;
    if (u==1) {
    if (i>=10) cout << "Библиотека переполнена.\n"; else {
    i++;
    cout << "Введите данные о книге:\n";
    cout << "Введите название книги:\n";
    cin >> a[i].name;
    cout << "Введите имя автора книги:\n";
    cin >> a[i].autor;
    cout << "Введите жанр книги:\n";
    cin >> a[i].genre;
    cout << "Введите год выпуска книги:\n";
    cin >> a[i].year;
    a[i].code=i;
    }
    }
    if (u==2) {
        if (i==0) cout << "В библиотеке пока нет книг.\n"; else {
        cout << "Введите название книги:\n";
        cin >> p;
        for (j=1;j<=i;j++) {
            if (a[j].name==p) {
                cout << "Книга '" << p << "'. Автор: " << a[j].autor << ". Жанр: " << a[j].genre << ". Год выпуска: " << a[j].year << ". Идентификатор книги в библиотеке: " << a[j].code << ".\n";
            }
            else cout << "Данной книги нет в библиотеке.";
        }
        }
    }
    if ((u!=1)&&(u!=2)&&(u!=3)) cout << "Введён некорректный символ.";
    } while (u!=3);
    cout << "До свидания!\n";
    return 0;
}

Практическая работа 4. Вариант 3.

#include <iostream>
#include "locale"

using namespace std;

void zap(int n,int m,int **mas) {
int i,j;
for (i=0;i<n;i++)
    for (j=0;j<m;j++)
       mas[i][j]=10 + rand() % 41 ;
}

void vyv(int n,int m,int **mas) {
int i,j;
for (i=0;i<n;i++) {
    for (j=0;j<m;j++) {
        cout << mas[i][j] << " ";
    }
    cout << "\n";
}
}

int main()
{
setlocale(LC_ALL,"Russian");

int n,m;
cout << "Введите количество строк: ";
cin >> n;
cout << "\nВведите количество столбцов: ";
cin >> m;
cout << "\n";
int **mas=new int*[n];
for (int l=0;l<m;l++)
        mas[l] = new int[m];

zap(n,m,mas);
vyv(n,m,mas);

delete [] mas;
    return 0;
}

Практическая работа 5, вариант 4.

#include <iostream>
#include <cmath>
#include <typeinfo>
#include "locale"
using namespace std;

void calc(int n, char c, int m){
switch (c){
          case '+': cout << n << c << m << "=" << (n+m) << endl; break;
          case '-': cout << n << c << m << "=" << (n-m) << endl; break;
          case '/': cout << n << c << m << "=" << (n/m) << endl; break;
          case '*': cout << n << c << m << "=" << (n*m) << endl; break;
          case '^': cout << n << c << m << "=" << pow(n,m) << endl; break;
          default: cout<<"Такой операции нет"<< endl;
         }
}
void calc(double n, char c, double m){
switch (c){
          case '+': cout << n << c << m << "=" << (n+m) << endl; break;
          case '-': cout << n << c << m << "=" << (n-m) << endl; break;
          case '/': cout << n << c << m << "=" << (n/m) << endl; break;
          case '*': cout << n << c << m << "=" << (n*m) << endl; break;
          case '^': cout << n << c << m << "=" << pow(n,m) << endl; break;
          default: cout<<"Такой операции нет"<< endl;
         }
}
void calc(double n, char c, int m){
switch (c){
          case '+': cout << n << c << m << "=" << (n+m) << endl; break;
          case '-': cout << n << c << m << "=" << (n-m) << endl; break;
          case '/': cout << n << c << m << "=" << (n/m) << endl; break;
          case '*': cout << n << c << m << "=" << (n*m) << endl; break;
          case '^': cout << n << c << m << "=" << pow(n,m) << endl; break;
          default: cout<<"Такой операции нет"<< endl;
         }
}
void calc(int n, char c, double m){
switch (c){
          case '+': cout << n << c << m << "=" << (n+m) << endl; break;
          case '-': cout << n << c << m << "=" << (n-m) << endl; break;
          case '/': cout << n << c << m << "=" << (n/m) << endl; break;
          case '*': cout << n << c << m << "=" << (n*m) << endl; break;
          case '^': cout << n << c << m << "=" << pow(n,m) << endl; break;
          default: cout<<"Такой операции нет"<< endl;
         }
}
int main(){
    char a;
    string c,b;
    int i,p=0,r=0,xi,yi;
    double xd,yd;
    setlocale(LC_ALL,"Russian");

   cout<<"Введите первый операнд: \n";
   cin>>c;
   cout<<"Введите знак операции: \n";
   cin>>a;
   cout<<"Введите второй операнд:\n";
   cin>>b;

   for (i=0;i<c.length();i++) {
     if (c[i]=='.')  p=1;
   }
   if (p==0) xi=stoi(c); else xd=stod(c);

   for (i=0;i<b.length();i++) {
    if (b[i]=='.')  r=1;
   }
    if (r==0) yi=stoi(b); else yd=stod(b);

   if ((p==0)&&(r==0)) calc(xi,a,yi);
   if ((p==0)&&(r==1)) calc(xi,a,yd);
   if ((p==1)&&(r==0)) calc(xd,a,yi);
   if ((p==1)&&(r==1)) calc(xd,a,yd);

   return 0;
}


Практическая работа 6. Вариант 1. 

Файл Property.h

#ifndef PROPERTY_H
#define PROPERTY_H
class Property
{
    public:
        Property();
        virtual ~Property();
        Property(double);
        virtual double bill() = 0;
    protected:
        double worth;
};
#endif

Файл Property.cpp

#include "Property.h"
Property::Property() {}
Property::~Property() {}
Property::Property(double worth) {
	this->worth = worth;
}

Файл Appartment.h

#ifndef APPARTMENT_H
#define APPARTMENT_H
#include "Property.h"
class Appartment : public Property {
public:
    Appartment();
	Appartment(double);
	double bill() override;
	~Appartment();
};
#endif

Файл Appartment.cpp

#include "Appartment.h"
Appartment::Appartment(){}
Appartment::~Appartment() {}
Appartment::Appartment(double worth):Property(worth){}
double Appartment::bill() {
	return worth/1000;
}

Файл Car.h

#ifndef CAR_H
#define CAR_H
#include "Property.h"
class Car : public Property {
    public:
        Car();
        virtual ~Car();
        Car(double);
        double bill() override;
};
#endif

Файл Car.cpp

#include "Car.h"
Car::Car() {}
Car::~Car() {}
Car::Car(double worth):Property::Property(worth){}
double Car::bill() {
	return worth / 200;
}

Файл CountryHouse.h

#ifndef COUNTRYHOUSE_H
#define COUNTRYHOUSE_H
#include "Property.h"
class CountryHouse : public Property {
    public:
        CountryHouse();
        virtual ~CountryHouse();
        CountryHouse(double);
        double bill() override;
};
#endif

Файл CountryHouse.cpp

#include "CountryHouse.h"
CountryHouse::CountryHouse(double worth):Property::Property(worth){}
double CountryHouse::bill() {
	return worth / 500;
}
CountryHouse::CountryHouse() {}
CountryHouse::~CountryHouse() {}

Файл main.cpp

#include <iostream>
#include "Property.h"
#include "Appartment.h"
#include "Car.h"
#include "CountryHouse.h"
#include "locale"
using namespace std;
int main()
{
  setlocale(LC_ALL,"Russian");
	Property **property=new Property*[7];
	property[0]=&Appartment(1000000);
	property[1]=&Appartment(2000000);
	property[2]=&Appartment(3000000);
	property[3]=&Car(400000);
	property[4]=&Car(500000);
	property[5]=&CountryHouse(6000000);
	property[6]=&CountryHouse(7000000);
  double sum = 0;
  for (int i = 0; i < 7; i++) {
	  sum += property[i]->bill();
	}
  cout << "К оплате счетов: " << sum;
  delete(property);
}
	

Практическая работа 8. Вариант 2.

#include <iostream>
#include <fstream>
#include <Windows.h>
#include "string"
#include "locale"
using namespace std;

int main()
{
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);
    setlocale(LC_ALL,"Rus");
    char s[256];
    ofstream F("C:\\Users\\ASUS\\Desktop\\oop\\prak\\8\\pr8.txt");
    cout << "Введите текст: \n";
    cin.getline(s,256);
    F << s;
    cout << "Текст записан в файл.\n";
    F.close();
    return 0;
}
