# php-puzzles

Задачки по php

## Среда для решения задач

1. Настроить локальный php для работы [assert](https://www.php.net/manual/ru/function.assert.php)
2. Воспользоваться готовой средой в Docker. [Репозиторий](https://github.com/otis22/php-minimal), [Видео инструкция](https://www.loom.com/share/e7434b8cd8fa4b0da69a8c0cf0339aa1)
3. Воспользоваться [сервисом](https://sandbox.onlinephpfunctions.com/)


## Как выполнять задачи

Написание всех функций начинать с написания набора asserts.

**Например:** Напишите функцию рассчета факториала числа n. 

Решение:
1. Пишем решение в любой среде, в которой работает функция `assert`
2. Пишем объявление функции и утверждения 
```php
function factorial($n)
{

}
assert(factorial(0) == 1);
assert(factorial(1) == 1);
assert(factorial(4) == 24);
```
3. Запускаем скрипт и убеждаемся, что он падает из-за проваленных assert
4. Пишем тело функции и чиним все ассерты
5. Код на ревью отправляем в личных сообщениях. Описываем какие задачи решались и набор ссыллок с онлайн сервиса или ссылку на репозиторий в github с комментариями где искать решение.
6. Если код проверен, присылаем pull request с своим именем(ником или ФИО) в список тех кто сделал

### Как писать утверждения? 

Пример задачи: 

> Напишите функцию count_even(array $arr): int, которая считает количество четных чисел в массиве и возвращает их количество. В массиве [1, 2, 3] - только 1 четный элемент, функция вернет 1.

Мы должны проверить, что функция работает верно. Первый тест описан прям в условии. 

1. Массив из условия, должен отдавать 1. Записываем.

```php
assert(count_even([1, 2, 3]) === 1);
```

Придумаем свои случаи: 

2. Массив подлинеее

```php
assert(count_even([1, 2, 3, 4, 5, 6, 7]) === 3) //  у нас четные это 2, 4, 6
```

3.  Пустой массив

```php
assert(count_even([]) === 0) 
```

4. Массив без четных

```php
assert(count_even([1, 3, 5, 7, 9]) === 0)
```

Этого достаточно для хорошего решения задачи. Дальше можно искать маньяков, которые передадут не массив, массив строк, массив из чисел и строк и отдельно продумывать как наша функция должна себя вести и тестировать это поведение, но этого уже нет в условии задачи.

## Puzzles 

* [1](puzzles/1.md)
* [2](puzzles/2.md)
