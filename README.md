# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
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
- ✨Magic ✨

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1
### Измените параметры файла. yaml-агента и определить какие параметры и как влияют на обучение модели:
Ход работы:
1) Скачал и установил предложенный проект, к нему подключил Mlagent и докачал нужные пакеты. 
![1](https://user-images.githubusercontent.com/113898917/204819183-b67ec5df-9396-4611-b3f6-28919184e651.png)


![2](https://user-images.githubusercontent.com/113898917/204819208-3eb8ecfe-b27a-4f59-90ca-253c568ba2df.png)


![3](https://user-images.githubusercontent.com/113898917/204819223-24e365cc-3ede-40f9-be11-8a2758d5fc95.png)


![4](https://user-images.githubusercontent.com/113898917/204819236-146d2c48-0041-40b3-bb10-b71fa7a1d683.png)


![5](https://user-images.githubusercontent.com/113898917/204819245-bb5d5ce1-5374-463f-aa47-6e34f4d1e8bf.png)

На 6-м же скриншоте можно посмотреть на результаты обучения для 12 одновременно существующих моделей:
![6!!!](https://user-images.githubusercontent.com/113898917/204819257-2c1f144b-dc59-44ed-b05f-3d773074d8ab.png)

2) Подключил TensorBoard и открыл для стандартных значений:
![start2](https://user-images.githubusercontent.com/113898917/204826862-2e91d56b-34b8-41f6-91ec-4fe7c168eea8.png)

3) Далее попробовал менять значения переменных в файле Economic для выявления различий в результатах:
   1. Сменил lambd: 0.95 на 0.5:
   ![lambd2](https://user-images.githubusercontent.com/113898917/204827273-43d86900-a9b6-4024-b897-4d39285e6d1c.png)                                  
   Данная переменная используется при расчете обобщенной оценки преимущества 'GAE'.
   2. Сменил epsilon: 0.2 на 0.4:
   ![epsilon](https://user-images.githubusercontent.com/113898917/204833358-49c8e16d-9065-4d21-b95f-cb88cbf7c66b.png)                                  
   Данная переменная используется при расчете быстроты развития политики во время обучения.
   3. Сменил learning_rate: 3.0e-4 на 2.0e-6:
   ![learningRate](https://user-images.githubusercontent.com/113898917/204835474-b3022a47-1c33-4900-a3af-7c9df8579099.png)                                 
   Данная переменная используется при расчете начальной скорости обучения.


## Задание 2
### Опишите результаты, выведенные в TensorBoard:
   Данные графики из категории Environment представляют из себя:

   Cumulative reward отвечает за среднее вознаграждение в эпоху для всех агентов (в нашем случае 1 эпоха = 5000 шагов), это накопительный график поэтому вознаграждение должно увеличиваться со временем, однако могут появляться "проседания" в графике. Так же иногда для наглядности результата может потребоваться пройти огромное кол-во шагов.
   Episode Length показывает cреднюю длительность каждой эпохи для всех агентов в данной среде.
   Policy Loss показывает среднюю величину функции, отвечающей за то, насколько сильно меняется процесс принятия решений, значения данной функции могут колебаться, но обычно должны быть меньше одного, кроме того, тренировка считается успешной, если разброс значений уменьшается со временем.
   Value Loss показывает cреднюю потерю обновлений функции значения. В общем, данный график должен возрастать, пока млАгент обучается, а потом убывать, когда вознаграждение придет в норму. Соответствует тому, насколько модель в состоянии 'предсказать' значения следующих состояний.
## Выводы
   1. Я еще раз потренировался в подключении mlAgent'a к проекту, а также других его дополнений. Кроме того, я попробовал впервые установить TensorBoard и проанализировать взятые оттуда графики.
   2. Далее, изменив значения переменных в .yaml файле, отвечающем за обучение агента, я заметил разницу в значениях на графиках, откуда сделал вывод, что обучение агента, его стабильность, точность, хаотичность и, что самое главное, скорость может варьироваться в зависимости от значений переменных, переданных в вышеупомянутом файле
   3. Также, познакомился с возможностью представления экономической системы игр (и не только) с помощью Unity.
