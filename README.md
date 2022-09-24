# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил(а):
- Береснев Егор Максимович
- РИ210910
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### Написать программы Hello World на Python и Unity:
Ход работы:
1) Код и вывод программы на языке Python:
![Hello, world](https://user-images.githubusercontent.com/113898917/191014932-474e8c5d-24e3-4828-a898-684c7d4da499.png)
2) Для Unity:  
      сначала создаем новый объект, в нем в Assets создаем C# Script и, открыв его, пишем код для вывода Hello, world!
![1](https://user-images.githubusercontent.com/113898917/191026982-810ce39b-d4f0-407e-96d0-31c9c4b71fd6.png)
      затем в Unity, добавляем наш скрипт в пустой объект и запускаем
![Unity 2](https://user-images.githubusercontent.com/113898917/191026989-50ae3a3c-2a19-48cd-a856-fd43d50f105f.png)


## Задание 2
### В разделе "Ход работы" пошагово выполнить каждый пункт с описанием и примеров реализации задачи по теме лабораторной работы.
- Произвел подготовку данных для работы с алгоритмом линейной регрессии
![image](https://user-images.githubusercontent.com/113898917/192098163-453fc43c-ea8e-44df-9c07-747142dd7134.png)

- Определил связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: метод градиентного спуска для нахождения частных производных w и b.
![image](https://user-images.githubusercontent.com/113898917/192098707-014e7ed4-9f05-4e8c-bd07-25e133123a87.png)

- Начал итерацию. Шаг 1. Инициализация и модель итеративной оптимизации.
![image](https://user-images.githubusercontent.com/113898917/192098926-31e0f4e5-c0ce-43b7-9801-3f7702c4302f.png)

- Шаг 2. На второй итерации отображается значения параметров, значения потерь и эффекты визулизации после итерации:
![image](https://user-images.githubusercontent.com/113898917/192099014-29fe0944-5259-4c11-b03d-b1a9863ffd2b.png)

- Шаг 3. Третья итерация показывает значения параметров, значения потерь и визуализацию после итерации:
![image](https://user-images.githubusercontent.com/113898917/192099072-fe013bf9-8859-4e6e-a5a0-6e65388b02e6.png)

- Шаг 4. На четвёртой итерации отображаются значения параметров, значения потерь и эффекты визулизации:
![image](https://user-images.githubusercontent.com/113898917/192099123-7182ba5a-dd8c-4c85-b42a-e7842f32e3f6.png)

- Шаг 5. Пятая итерация показывает значение параметра, значение потерь и эффект визуализации после итерации:
![image](https://user-images.githubusercontent.com/113898917/192099132-436bfc1d-6cf0-41b4-8bab-41920348afb8.png)

- Шаг 6. 10000-я итерация, показывающая значение параметров, потери и визуализацию после итерации:
![image](https://user-images.githubusercontent.com/113898917/192099146-1bc35228-8648-432e-ae0c-aa69f19ac676.png)

- В ходе выполнения программы появится график:
![image](https://user-images.githubusercontent.com/113898917/192099270-eddb41ea-d66d-4a05-9692-4cca0f26e72b.png)


## Задание 3
### Изучить код на Python и ответить на вопросы:


## Выводы


