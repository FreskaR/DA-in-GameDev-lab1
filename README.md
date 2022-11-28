# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Береснев Егор Максимович
- РИ210910
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

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

## Цель работы
Ознакомиться с принципом работы Перцептрона.

## Задание 1
### В проекте Unity реализовать перцептрон, которые умеет проводить операции OR, AND, NAND, XOR:
   ### Ход работы:
   1) Скачал файл со скриптом перцептрона и добавил его к GameObject'у в новом 2d проекте в Unity:   
![Adding Perceptron](https://user-images.githubusercontent.com/113898917/204292176-f64ca585-04f5-4d2d-a00f-4dcab58c2e53.png)
   2) Установил значения, подходящие к логической операции OR в настройках перцептрона: 
![OR](https://user-images.githubusercontent.com/113898917/204292304-6faeda14-947e-4459-b102-cb32b688ac08.png)
      
   2.1) Попробовал запустить его, установив значение для Train: 1, 2, 3, 4, 5, 6, 8, 10:
![OR1](https://user-images.githubusercontent.com/113898917/204292796-52ba9f6c-c31b-4975-8d47-d5d185232b35.png)
 ^ для 1 эпохи на выходе было 3 ошибки.
![OR2](https://user-images.githubusercontent.com/113898917/204292900-362d32e1-fd31-44bf-bc48-176335f35191.png)
^ для 2 эпох сначала 1-а ошибка, затем 2-е.
![OR3](https://user-images.githubusercontent.com/113898917/204293060-5dbf0f9c-3519-4c9c-b401-60d6f68cc3e1.png)
^ на третьей эпохе в конце была всего 1 ошибка
![OR4](https://user-images.githubusercontent.com/113898917/204293162-9fdea835-776b-43a2-9957-e84ce89bad71.png)
^ начиная с 4-й перцептрон заканчивал работу без ошибок.
![OR5](https://user-images.githubusercontent.com/113898917/204293250-0d0a9f3e-22db-48fe-8717-b3394230ccb1.png)
![OR6](https://user-images.githubusercontent.com/113898917/204293255-64dc411c-c403-4dfb-b02a-9c2a3039d03c.png)
![OR8](https://user-images.githubusercontent.com/113898917/204293266-c7a7710c-e9ec-4c5a-9deb-452a806852d4.png)
![OR10](https://user-images.githubusercontent.com/113898917/204293273-ee2f2705-d4f5-4e59-9dc7-5beb01180f84.png)
   3) Установил значения в настройках для операции AND:
 ![AND](https://user-images.githubusercontent.com/113898917/204297566-e328c47c-1422-48d8-89c5-649be9e2770e.png)
   далее пробовал подставить разные значения эпох:
  ![AND1](https://user-images.githubusercontent.com/113898917/204297663-5d22fad4-0c22-4bcf-acf6-f7948a9c7cdc.png)
![AND2](https://user-images.githubusercontent.com/113898917/204297685-b696b1a5-cf27-440a-8c20-04e1ebf4bd89.png)
![AND3](https://user-images.githubusercontent.com/113898917/204297692-0cdb566d-e603-428f-ac61-67e2dc58d67f.png)
![AND5-1](https://user-images.githubusercontent.com/113898917/204297714-8e146c34-abff-443f-985d-44afe838adac.png)
![AND5-2](https://user-images.githubusercontent.com/113898917/204297734-e84f33ea-ab79-4df4-bbaf-a615f557bcdf.png)
![AND6](https://user-images.githubusercontent.com/113898917/204297738-c5f89aeb-0463-4ff8-b2ca-1589d017ac32.png)
^ с 1-й по 4-ю кол-во ошибок варьировалось около 2-3-х, на 5 эпохе иногда проходил без ошибок, иногда с ошибками, а начиная с 6 все случаи, когда я проверял, заканчивал без ошибок.
   4) Установил значения в настройках для операции NAND:
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
![image](https://user-images.githubusercontent.com/113898917/192099932-4abd5aef-130d-4f0f-b1da-7c8e50e748a5.png)


## Задание 3
### Изучить код на Python и ответить на вопросы:
   
   
  - Вопрос 1: Должна ли величина loss стремиться к нулю при изменении исходных данных? Приведите пример выполнения кода, который подтверждает ваш ответ.
    
    Ответ: величина loss МОЖЕТ стремиться к нулю в двух случаях:
    
    1. Использовалась линейная функция, например: y = x, a = 1, b = 0
    ![image](https://user-images.githubusercontent.com/113898917/192100217-e0a10901-91c1-48ba-91fa-d3233c72b057.png)
    
    2. Значения x и y стремятся к нулю:
    ![Screenshot_1](https://user-images.githubusercontent.com/113898917/192100473-8d1115b6-0194-4643-bfb8-1c51811db34a.png)
  - Вопрос 2: Какова роль параметра Lr? Приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.
    
    Ответ: Этот параметр отвечает за значения a, b, loss и их изменения, так: чем меньше Lr, тем сильнее будет меняться loss и слабее a, b, отсюда же следует и обратное: чем больше Lr, тем слабее будет меняться loss и сильнее a, b (Короче говоря, Lr определяет точность графика)
    
    При Lr = 0,0000001:
    ![image](https://user-images.githubusercontent.com/113898917/192100719-05da1684-1f05-4054-a9c8-67637b0e1e4b.png)
    
    При Lr = 0,001:
    ![image](https://user-images.githubusercontent.com/113898917/192100735-19d6a8aa-92f9-495b-a957-b02acfaad4c2.png)

## Выводы
   1. Установил и настроил нужное для дальнейшего обучения ПО: unity, VS Code, Pycharm
   2. В Unity и Pycharm написаны и выведены "Hello world!"
   3. Смог проанализировать работу программы на примере предложенного кода линейной регрессии
