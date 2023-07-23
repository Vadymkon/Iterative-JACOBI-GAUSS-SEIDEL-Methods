#include <iostream>
#include <vector>
#include <stdlib.h> // max
using namespace std;
double E = 0.0001;
double x1, x2, x3;
double SAFEx1, SAFEx2, SAFEx3;
vector <double> x1TAB, x2TAB, x3TAB; //сюда будем писать историю
итерации, для вывода
//start --- vector <double> first{ 3.2, -2.5, 3.7, 6.5 }, second{ 0.5, 0.34, 1.7,
-0.24 }, third{ 1.6, 2.3, -1.5, 4.3 };
vector <double> first{ 4.8 , 2.2, -0.2, 10.8 }, second{ 0.5, 1.7, 0.34, -0.24 },
third{ 2.1, 0.2, 2.64, 4.06};
// ax1 + bx2 + cx3 = d; это коефы [a,b,c,d] ,
// что {0,1,2,3}
void x_calc()
{
SAFEx1 = x1; x1TAB.push_back(SAFEx1);
SAFEx2 = x2; x2TAB.push_back(SAFEx2);
SAFEx3 = x3; x3TAB.push_back(SAFEx3);
x1 = (first[3] - first[1] * SAFEx2 - first[2] * SAFEx3) / first[0];
//а это уравнение x1 = (d - bx2 - cx3) / a
x2 = (second[3] - second[0] * SAFEx1 - second[2] * SAFEx3) /
second[1];
//а это уравнение x2 = (d - ax1 - cx3) / b
x3 = (third[3] - third[1] * SAFEx2 - third[0] * SAFEx1) / third[2];
//а это уравнение x3 = (d - bx2 - ax1) / c
}
//даёт нам новые иксы и в сейве старые иксы
double justFUNCTION(vector <double> sho)
{
return sho[0] * x1 + sho[1] * x2 + sho[2] * x3;
}
void printQ(vector <double> first)
{
cout << first[0] << "x1 + " << first[1] << "x2 + " << first[2] << "x3 = " <<
first[3] << endl;
}
//банальный вывод для проверки уравнений
void uslovieALL()
{
bool a, b, c;
if ((abs(first[1]) + abs(first[2])) / abs(first[0]) > 1)
{
cout << "errMOMENT 1 " << (abs(first[1]) + abs(first[2])) /
abs(first[0]) << endl;
a = true;
}
else a = false;
//проверка первого уравнения
if ((abs(second[0]) + abs(second[2])) / abs(second[1]) > 1)
{
cout << "errMOMENT 2 " << (abs(second[0]) + abs(second[2]))
<< endl;
b = true;
}
else b = false;
//проверка второго уравнения
if ((abs(third[1]) + abs(third[0])) / abs(third[2]) > 1)
{
cout << "errMOMENT 3 " << (abs(third[1]) + abs(third[0])) <<
endl;
c = true;
}
else c = false;
//проверка третьего уравнения
if (
a == true
||
b == true
||
c == true
)
{
cout << endl << "KOEFS are invalid." << endl;
}
}
//проверка всех уравнений
int main()
{
uslovieALL(); //выводит сообщение, если коэфициенты
неподходящие, и показывает где конкретно трабблы
//x(0) - нулевая итерация
x1 = first[3];
x2 = second[3];
x3 = third[3];
int limitation = 0;
while
(
abs( x1 - SAFEx1 ) >= E
&
abs( x2 - SAFEx2 ) >= E
&
abs( x3 - SAFEx3 ) >= E
) //условием повтора - является проверка точности
{
x_calc(); //подсчёт иксов
limitation += 1;//для пункта 3(бесполезная штука)
if (limitation > 20)
{
cout << "\nmax limit of limitations ERROR" << endl;
exit(0);
}
}
x1TAB.push_back(SAFEx1);
x2TAB.push_back(SAFEx2);
x3TAB.push_back(SAFEx3);
//запись последних иксов (последней итерации)
//вывод
cout << "\n" << "0" << " iteration\t" << "x1 = " << x1TAB[0] << "\tx2 = "
<< x2TAB[0] << "\tx3 = " << x3TAB[0]; //отдельно для нулевого
for (int i = 1; i < x1TAB.size(); i++)
{
cout << "\n" << i << " iteration\t" << "x1 = " << x1TAB[i] << "\tx2 = "
<< x2TAB[i] << "\tx3 = " << x3TAB[i]
<< "\tFLUFF = " << max(max(abs(x1TAB[i] - x1TAB[i - 1]),
abs(x2TAB[i] - x2TAB[i - 1])), abs(x3TAB[i] - x3TAB[i - 1]))
;
}
//невязка (пункт 6)
cout << "\nfirst: " << justFUNCTION(first) << "\t real be === " << first[3]
<< "\t NEVAZKA: " << abs(justFUNCTION(first) - first[3])
<< "\nsecond: " << justFUNCTION(second) << "\t real be === "
<< second[3] << "\t NEVAZKA: " << abs(justFUNCTION(second) - second[3])
<< "\nthird: " << justFUNCTION(third) << "\t real be === " <<
third[3] << "\t NEVAZKA: " << abs(justFUNCTION(third)- third[3]);
}

void x_calc()
{
SAFEx1 = x1; x1TAB.push_back(x1);
SAFEx2 = x2; x2TAB.push_back(x2);
SAFEx3 = x3; x3TAB.push_back(x3);
x1 = (first[3] - first[1] * x2 - first[2] * x3) / first[0];
//а это уравнение x1 = (d - bx2 - cx3) / a
x2 = (second[3] - second[0] * x1 - second[2] * x3) / second[1];
//а это уравнение x2 = (d - ax1 - cx3) / b
x3 = (third[3] - third[1] * x2 - third[0] * x1) / third[2];
//а это уравнение x3 = (d - bx2 - ax1) / c
}
