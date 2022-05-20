# Домашнее задание к лекции «Открытие и чтение файла, запись в файл»
***

Необходимо написать программу для кулинарной книги.

Список рецептов должен храниться в отдельном файле в следующем формате:

```Название блюда
Количество ингредиентов в блюде
Название ингредиента | Количество | Единица измерения
Название ингредиента | Количество | Единица измерения
...
```
### Пример(файл в папке files):
```
Омлет
3
Яйцо | 2 | шт
Молоко | 100 | мл
Помидор | 2 | шт

Утка по-пекински
4
Утка | 1 | шт
Вода | 2 | л
Мед | 3 | ст.л
Соевый соус | 60 | мл

Запеченный картофель
3
Картофель | 1 | кг
Чеснок | 3 | зубч
Сыр гауда | 100 | г

Фахитос
5
Говядина | 500 | г
Перец сладкий | 1 | шт
Лаваш | 2 | шт
Винный уксус | 1 | ст.л
Помидор | 2 | шт
```
* В одном файле может быть произвольное количество блюд.
* Читать список рецептов из этого файла.
* Соблюдайте кодстайл, разбивайте новую логику на функции и не используйте глобальных переменных.
### Задача №1
***

Должен получится следующий словарь
```
cook_book = {
  'Омлет': [
    {'ingredient_name': 'Яйцо', 'quantity': 2, 'measure': 'шт.'},
    {'ingredient_name': 'Молоко', 'quantity': 100, 'measure': 'мл'},
    {'ingredient_name': 'Помидор', 'quantity': 2, 'measure': 'шт'}
    ],
  'Утка по-пекински': [
    {'ingredient_name': 'Утка', 'quantity': 1, 'measure': 'шт'},
    {'ingredient_name': 'Вода', 'quantity': 2, 'measure': 'л'},
    {'ingredient_name': 'Мед', 'quantity': 3, 'measure': 'ст.л'},
    {'ingredient_name': 'Соевый соус', 'quantity': 60, 'measure': 'мл'}
    ],
  'Запеченный картофель': [
    {'ingredient_name': 'Картофель', 'quantity': 1, 'measure': 'кг'},
    {'ingredient_name': 'Чеснок', 'quantity': 3, 'measure': 'зубч'},
    {'ingredient_name': 'Сыр гауда', 'quantity': 100, 'measure': 'г'},
    ]
  }
```
### Задача №2
***

Нужно написать функцию, которая на вход принимает список блюд из cook_book и количество персон для кого мы будем готовить

```<get_shop_list_by_dishes(dishes, person_count)```

На выходе мы должны получить словарь с названием ингредиентов и его количества для блюда. Например, для такого вызова

```get_shop_list_by_dishes(['Запеченный картофель', 'Омлет'], 2)```

Должен быть следующий результат:

```
{
  'Картофель': {'measure': 'кг', 'quantity': 2},
  'Молоко': {'measure': 'мл', 'quantity': 200},
  'Помидор': {'measure': 'шт', 'quantity': 4},
  'Сыр гауда': {'measure': 'г', 'quantity': 200},
  'Яйцо': {'measure': 'шт', 'quantity': 4},
  'Чеснок': {'measure': 'зубч', 'quantity': 6}
}
```

Обратите внимание, что ингредиенты могут повторяться

### Задача №3
***

В папке лежит некоторое количество файлов. Считайте, что их количество и имена вам заранее известны, пример для выполнения домашней работы можно взять тут

Необходимо объединить их в один по следующим правилам:

1. Содержимое исходных файлов в результирующем файле должно быть отсортировано по количеству строк в них (то есть первым нужно записать файл с наименьшим количеством строк, а последним - с наибольшим)
2. Содержимое файла должно предваряться служебной информацией на 2-х строках: имя файла и количество строк в нем

**Пример** Даны файлы: 1.txt
```
Строка номер 1 файла номер 1
Строка номер 2 файла номер 1
```
2.txt
```
Строка номер 1 файла номер 2
```

Итоговый файл:
```
2.txt
1
Строка номер 1 файла номер 2
1.txt
2
Строка номер 1 файла номер 1
Строка номер 2 файла номер 1
```
### Задача №4
***

Для подготовки к следующей лекции прочитайте про менеджер контекста.

***
### Как сдавать задачи

Пишите код в IDE (рекомендуем Pycharm, версия Community, инструкцию по установке вы найдете на сайте).

* Почему лучше работать в IDE? — Ускоряет работу, есть подсветка ошибок, отладка по шагам.
* Для более подробной информации изучите инструкцию по работе с Pycharm.
* Опирайтесь на принятые правила оформления кода, чтобы выработать привычку писать профессионально. При несоблюдении принятого стиля домашние задания могут быть отправлены на доработку.
1. Инициализируйте на своём компьютере пустой Git-репозиторий
2. Добавьте в этот же каталог необходимые файлы
3. Сделайте необходимые коммиты
4. Создайте публичный репозиторий на GitHub и свяжите свой локальный репозиторий с удалённым
5. Сделайте пуш (удостоверьтесь, что ваш код появился на GitHub)
6. Ссылку на ваш проект отправьте в личном кабинете на сайте netology.ru
7. Задачи, отмеченные как необязательные, можно не сдавать, это не повлияет на получение зачета (в этом ДЗ все задачи являются обязательными)
8. Любые вопросы по решению задач задавайте в чате Slack, но мы не сможем проверить или помочь, если вы пришлете:
* архивы;
* скриншоты кода;
* теоретический рассказ о возникших проблемах.