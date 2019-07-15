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
int int8 int16 int32 int64 float double
### Прочие
void -> пустой тип
string -> строка юникодных символов 
bool -> синоним int8
char -> символ
array -> массив переменной длины std::vector
set -> множество
## Стандартные функции
### Общие
print(string s) void -> печатает на экран строку s  
input() string -> возвращает ввод пользователя
### Математические
abs(number n) number -> возвращает модуль числа n  
sqrt(number n) number -> возвращает корень числа n  
hypot(number a,number b) number -> возвращает гипотенузу c^2=a^2+b^2    
max(array[number] arr) number -> возвращает максимальный элемент массива arr   
min(array[number] arr) number -> возвращает минимальный элемент массива arr  
sum(array[number] arr) number -> возвращает сумму элементов массива arr  
prod(array[number] arr) number -> возвращает произведение элементов массива arr  
round(number n) number ->  окгуляет число n по правилу "школьного" округления  
bround(number n) number -> округляет число n (банковское округление)  
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
g -> Усорение свободного падения   
G -> Гравитационная постоянная  
c -> Скорость света  
h -> постоянная Планка  
k -> постоянная Больцмана  
F -> постоянная Фарадея  
Na -> число Авогадро
