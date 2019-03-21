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
