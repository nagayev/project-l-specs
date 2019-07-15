# Project-L документация

## Введение
### Система сокращений
number как тип означает, что функция может принимать как аргумент любой числовой тип.

### Формат документации
Для функций и переменных
название_функции(тип аргумент,...) тип возврата -> что возвращает функция  
Например:  
abs(int n) int -> Возвращает модуль числа n
## Стандартные типы данных
### Числовые
int int8 int16 int32 int64  
uint uint8 uint16 uint64  
float double  
complex  
### Прочие
void -> пустой тип  
string -> строка юникодных символов   
bool -> булева значение, синоним int8  
char -> символ  
array -> массив переменной длины std::vector   
date -> дата, синоним int64  
set -> множество  
## Стандартные функции
### Общие
print(string s) void -> печатает на экран строку s  
input() string -> возвращает ввод пользователя  
exit(int code) void -> завершает приложение с кодом code  
### Математические
abs(number n) number -> возвращает модуль числа n  
sqrt(number n) number -> возвращает корень числа n  
hypot(number a, number b) number -> возвращает гипотенузу c^2=a^2+b^2    
max(array[number] arr) number -> возвращает максимальный элемент массива arr   
min(array[number] arr) number -> возвращает минимальный элемент массива arr  
sum(array[number] arr) number -> возвращает сумму элементов массива arr  
prod(array[number] arr) number -> возвращает произведение элементов массива arr  
round(number n) number ->  окгуляет число n по правилу "школьного" округления  
bround(number n) number -> округляет число n (банковское округление)  
rand() float -> возвращает случайное число от 0 до 1  
randbtw(number a, number b) float -> возвращает случайное число от a до b  
ceil(number n) number -> округление вверх   
floor(number n) number ->  округление вниз  
trunc(number n) number -> усекает число n до ближайшего целого
exp(number n) number ->  
ln(number n) number -> натуральный логарифм числа n  
log(n,base) number -> логарифм числа n по основанию base  
sin(number n) number -> синус числа n   
cos(number n) number -> косинус числа n   
tan,tg(number n) number -> тангенс числа n   
ctg(number n) number -> котангенс числа n    
sec(number n) number ->  секанс числа n  
cosec(number n) number -> косеканс числа n    
arcsin,asin(number n) number -> арксинус числа n     
arccos,acos(number n) number -> арккосинус числа n   
arctg,atan(number n) number -> арктангенс числа n      
arcctg(number n) number -> аркотангенс числа n  
## Стандартные константы
true -> 1  
false -> 0  
pi -> Число Пи  
e -> Число Эйлера, основание натурального логарифма  
tau -> Число тау, 2*pi  
g -> Ускорение свободного падения   
G -> Гравитационная постоянная  
c -> Скорость света  
h -> постоянная Планка  
k -> постоянная Больцмана  
F -> постоянная Фарадея  
Na -> число Авогадро
## Работа с множествами
isSubset(set a, set b) bool -> возвращает true, если все элементы a принадлежат b  
difference(set a, set b) set -> возвращает множество уникальных элементов a  
union(set a, set b) set -> объединение множеств a и b, a|b  
intersection(set a, set b) set -> пересечение a и b, a&b  
## Работа с датой и временем 
Тип date используется для хранения количества миллисекунд, прошедших с 1 января 1970 года 0:0:0  
В языке решена [Проблема 2038 года](https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%BE%D0%B1%D0%BB%D0%B5%D0%BC%D0%B0_2038_%D0%B3%D0%BE%D0%B4%D0%B0).  
Для операций над датой и временем доступны следующие функции:  
now() date -> возвращает количество миллисекунд с 1 января 1970 года.  
getYear(date d) int -> возвращает год    
getMonth(date d) int -> возвращает месяц  
getDate(date d) int -> возвращает число мемяца  
getDay(date d) int -> возвращает день недели  
isLeapYear(int year) bool -> возвращает true, если год высокосный, false в других случаях  
monthLength(int year, int month) int -> возвращает длину месяца month в годе year  
diffTime(date end, date start) date -> возвращает разницу в миллисекундах между end и start
<!--`date d=0; 
getYear(d); `
-->
