# oop imbo-01-18 практика

Сделать форк этого репозитория и загрузить к себе в репозиторий текст программы. 

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
