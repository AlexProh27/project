

#### 


# Стандартные библиотеки

#### В этом репозитории Вам представлены реализованные библиотеки s21_decimal.h, s21_math.h, s21_string.h на языке программирования Си. 
1. [Decimal.h](#part-1-установка-ос)
2. [Math.h](#part-2-создание-пользователя)
3. [String.h](#part-3-настройка-сети-ос)


## s21_decimal
Эта библиотека должна добавить возможность работы с типом "decimal", который отсутствует в стандарте языка. Тем не менее, этот тип критически важен для, например, финансовых расчетов, где недопустимы погрешности вычислений, свойственные типам с плавающей точкой. В рамках этого проекта предполагается знакомство с задачами обработки финансовой информации, погружение в вопросы внутреннего представления различных типов данных и закрепление структурного подхода. 

#### Информация 
Тип Decimal представляет десятичные числа в диапазоне от положительных 79,228,162,514,264,337,593,543,950,335 до отрицательных 79,228,162,514,264,337,593,543,950,335. Значение Decimal по умолчанию равно 0. Decimal подходит для финансовых расчетов, которые требуют большого количества значимых целых и дробных цифр и отсутствия ошибок округления. Этот тип не устраняет необходимость округления. Скорее, сводит к минимуму количество ошибок из-за округления. 
Когда результат деления и умножения передается методу округления, результат не страдает от потери точности. 
Decimal число - это значение с плавающей точкой, состоящее из знака, числового значения, где каждая цифра находится в диапазоне от 0 до 9, и коэффициента масштабирования, который указывает положение десятичной точки, разделяющей целые и дробные части числового значения. 
Двоичное представление Decimal состоит из 1-разрядного знака, 96-разрядного целого числа и коэффициента масштабирования, используемого для деления 96-разрядного целого числа и указания того, какая его часть является десятичной дробью. Коэффициент масштабирования неявно равен числу 10, возведенному в степень в диапазоне от 0 до 28. Следовательно, двоичное представление Decimal имеет вид ((от -2^96 до 2^96) / 10^(от 0 до 28)), где -(2^96-1) равно минимальному значению, а 2^96-1 равно максимальному значению. 
Коэффициент масштабирования также может сохранять любые конечные нули в Decimal. Эти конечные нули не влияют на значение в арифметических операциях или операциях сравнения. 
    
## MATH.H
 Эта библиотека реализует базовые математические операции, которые затем используются в различных алгоритмах. В рамках выполнения этого проекта предполагалось ознакомиться с основами вычислительных методов и закрепление подходов структурного программирования. 
#### Информация 
Математические операции на языке Си представляют собой группу функций в стандартной библиотеке языка программирования Си, реализующих основные математические функции. Все функции так или иначе используют числа с плавающей запятой. Различные стандарты C предоставляют различные, хотя и обратно совместимые, наборы функций. Любые функции, которые работают с углами, используют радианы в качестве единицы измерения угла. 

## String.h
В данном проекте нужно было разработать собственную реализацию библиотеки string.h на языке программирования Си с некоторыми дополнениями (с собственной реализацией функций sprintf и sscanf). Библиотека string.h является основной библиотекой языка Си по обработке строк. В рамках этого проекта предполагалось отработать задач на работу со строковыми данными и закрепление структурного подхода. 

#### Информация 
Язык программирования C содержит набор функций, реализующих операции со строками (символьными строками и строками байтов) в своей стандартной библиотеке. В ней поддерживаются различные операции, такие как копирование, конкатенация, маркировка и поиск. Для символьных строк в стандартной библиотеке существует правило о том, что строки должны заканчиваться терминирующим нуль-символом: строка из n символов представляется в виде массива из n + 1 элементов, последний из которых является символом "NULL".  
Единственная поддержка строк собственно в языке программирования С заключается в том, что компилятор преобразует строковые константы в кавычках в строки, заканчивающиеся нулем. 
    
