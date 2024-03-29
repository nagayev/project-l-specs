# Project-L документация

## Введение
### О проекте
Project-L это компилируемый язык программирования, созданный для применения в научных целях.  
Этот документ является стандартом.  
В данном языке программирования присутствуют средства для работы с файловой системой, датой и временем, операционной системой.  
Также язык включает в себя модули для различных отраслей науки. Например physics предназначенный для физиков и chemistry для химиков.  
Особый упор был сделан на математические функции языка. В стандартную библиотеку включены средства для работы с тригонометрическими и гиперболическими функциями, комплексными и гиперкомплексными числами, матрицами и т.д  
Все предложения по улучшению языку принимаются в разделе Issues.  
### Система сокращений
number как тип означает, что функция может принимать как аргумент любой числовой тип.

### Формат документации
Для функций и переменных
название_функции(тип аргумент,...) тип возврата -> что возвращает функция  
Например:  
abs(int n) int -> Возвращает модуль числа n
## Синтаксис языка
Язык имеет си подобный синтаксис.
Например, форма записи оператора ветвления(if):
if(condition){
//Делаем что-то
}
## Стандартные модули
time - модуль с методами для работы с временем  
physics - физический модуль     
chemistry - химический модуль  
c - низкоуровневый модуль для C функций
## Стандартные типы данных
### Числовые
int(natural) int8 int16 int32 int64  
uint uint8 uint16 uint64  
float(real) double  
complex  
### Прочие
void -> пустой тип  
string -> строка юникодных символов   
bool -> булева значение, синоним int8  
byte -> символ Юникода  
array -> массив переменной длины (аналог std::vector)   
vector -> математический вектор
date -> дата, синоним int64  
set -> множество  
## Стандартные функции
### Общие
print(string s) void -> печатает на экран строку s  
input() string -> возвращает ввод пользователя  
exit(int code) void -> завершает приложение с кодом code  
range(int start, int stop, int step) range -> возвращает арифметическую последовательность
map(array[type] arr, callback) array[type] -> применяет функцию callback ко всем элементам arr
filter(arra[type] arr, callback) array[type] -> фильтрует значения arr, аналог std::copy_if
all(array[type] arr) bool -> true, если все элементы true
any(array[type] arr) bool -> true, если хотя бы один элемент true
### Математические
abs(number n) number -> возвращает модуль числа n  
sqrt(number n) number -> возвращает корень числа n 
factorial(number n) number -> возвращает факторил числа n  
hypot(number a, number b) number -> возвращает гипотенузу c^2=a^2+b^2    
max(array[number] arr) number -> возвращает максимальный элемент массива arr   
min(array[number] arr) number -> возвращает минимальный элемент массива arr  
sum(array[number] arr) number -> возвращает сумму элементов массива arr  
prod(array[number] arr) number -> возвращает произведение элементов массива arr  
round(number n) number ->  окгуляет число n по правилу "школьного" округления  
bround(number n) number -> округляет число n (банковское округление)  
rand() float -> возвращает случайное число от 0 до 1  
randbtw(number a, number b) float -> возвращает случайное число от a до b  
isNan(float n) bool -> если n Nan возвращает true, иначе - false  
isInf(float n) bool -> если n бесконечность, возвращает true, иначе - false  
toDegress(float radians) float -> перевод радиан в градусы  
toRadians(float degress) float -> перевод градусов в радианы  
copySign(number a, number b) -> возвращает число a со знаком числа b  
ceil(number n) number -> округление вверх   
floor(number n) number ->  округление вниз  
trunc(number n) number -> усекает число n до ближайшего целого
exp(number n) number ->  экспонента (e^n)  
log(number n, number base) number -> логарифм числа n по основанию base   
ln(number n) number -> натуральный логарифм числа n  
log10(number n) number -> логарифм числа n по основанию 10  
log2(number n) number -> логарифм числа n по основанию 2  
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
sinh(number n) number -> гиперболический синус числа n  
cosh(number n) number -> гиперболический косинус числа n  
tanh(number n) number -> гиперболический тангенс числа n  
ctgh(number n) number -> гиперболический котангенс числа n  
## Стандартные константы
true -> 1  
false -> 0  
pi -> Число Пи  
e -> Число Эйлера, основание натурального логарифма  
tau -> Число Тау, 2*pi  
## Работа с множествами
isSubset(set a, set b) bool -> возвращает true, если все элементы a принадлежат b  
difference(set a, set b) set -> возвращает множество уникальных элементов a  
union(set a, set b) set -> объединение множеств a и b, a|b  
intersection(set a, set b) set -> пересечение a и b, a&b  
## Работа с датой и временем, модуль time
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
## Научно-оринтированные модули
### physics
#### Методы
ctof(number c) number -> Преобразует градусы Цельсия в градусы Фаренгейта  
ftoc(number c) number -> Преобразует градусы Фаренгейта в градусы Цельсия    
ctok(number c) number -> Преобразует градусы Цельсия в градусы Кельвина  
ktoc(number c) number -> Преобразует градусы Кельвина в градусы Цельсия  

#### Константы
g -> Ускорение свободного падения   
G -> Гравитационная постоянная  
c -> Скорость света  
h -> постоянная Планка  
k -> постоянная Больцмана  
F -> постоянная Фарадея  
Na -> число Авогадро
### chemistry
#### Методы  
getElementMass(number element) -> возвращает молярную массу элемента element    
getElementGroup(number element) -> возвращает группу элемента element  
getElementPeriod(number element) -> возвращает период элемента element
## Модуль c
Данный модуль предназначен для вызовов некоторых си функций в коде, где производительность и/или потребление памяти критичны.  
### Типы
size (size_t)
char
### Методы
malloc
free
