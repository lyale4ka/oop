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

