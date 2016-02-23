# Задание 6. Дракон Хартера-Хейтуэя
Написать программу, выполняющую построение дракона Хартера-Хейтуэя с помощью системы итерируемых функций (IFS).

## Метод построения
Задачу можно решить с помощью рекурсии.
* На каждом шаге функция принимает отрезок в виде координат двух крайних точек.
* Каждое из двух преобразований IFS генерирует по отрезку.
При этом достаточно произвести вычисления только для двух крайних точек исходного отрезка, т.к. в нашем случае IFS состоит из аффинных преобразований, которые переводят отрезок в отрезок.
* Каждый новый отрезок запускает новую ветку рекурсии.

![Построение](/images/ifs.png)

## Входные данные
* количество итераций `n`

## Описание IFS
### Первое преобразование IFS</span>
<code>x<sub>1</sub>' = 0.5x + 0.5y</code><br>
<code>y<sub>1</sub>' = -0.5x + 0.5y</code><br>
    
### Второе преобразование IFS</span>
<code>x<sub>2</sub>' = -0.5x + 0.5y - 1</code><br>
<code>y<sub>2</sub>' = -0.5x - 0.5y</code><br>

## Замечания
* Вследствие того, что описанная IFS является сжимающим отображением выбор начального отрезка не принципиален - результат при большом числе итераций будет одинаков.
* Хотя построение фрактала с помощью IFS реализовывается через рекурсию, здесь есть особенности. При вычислении любой точки нового поколения кривой используется только одна точка предыдущего поколения и одно из двух преобразований IFS.
    
![Дракон Хартера-Хейтуэя](/images/dragon.png)