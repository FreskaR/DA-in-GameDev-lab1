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
![NAND](https://user-images.githubusercontent.com/113898917/204307347-4deffd99-06d0-4c54-8e5b-50784a74c43c.png)
Для данной опервации ошибки пропали только к 7 эпохам, хотя на 3-й в одно из испытаний также выдало удачный 0:
![NAND1](https://user-images.githubusercontent.com/113898917/204307537-4022eb38-9740-4153-8bb6-4d5eba631f44.png)
![NAND2](https://user-images.githubusercontent.com/113898917/204307547-06618738-92e2-417a-94eb-3946a4df3dab.png)
![NAND3-1](https://user-images.githubusercontent.com/113898917/204307556-75b739dd-26f9-41ff-b4c3-9ab0ce57fe4b.png)
![NAND3-2](https://user-images.githubusercontent.com/113898917/204307567-fefa5d7b-ce24-4d4d-bd7f-796598fa3b0c.png)
![NAND4](https://user-images.githubusercontent.com/113898917/204307582-055d23b0-21d4-4117-a9f4-5f8618fc05ad.png)
![NAND6](https://user-images.githubusercontent.com/113898917/204307593-c738b966-15c0-4040-b711-3c08a63589de.png)
![NAND7](https://user-images.githubusercontent.com/113898917/204307609-06a980e1-0168-49d0-98f6-c26d17a38976.png)
   5) Установил значения в настройках для операции XOR:                                                                                 
   ![XOR](https://user-images.githubusercontent.com/113898917/204310702-6718ac62-f263-4ef9-9360-4c2bb35cac69.png)                           
   Данная операция начала заканчиваться без ошибок только к примерно 9 итерациям
![XOR1](https://user-images.githubusercontent.com/113898917/204310890-9d7a15e6-36a2-495c-a465-a15812c2521b.png)
![XOR3](https://user-images.githubusercontent.com/113898917/204310897-0e27be36-db5b-45db-a955-31015e6ce5e3.png)
![XOR5](https://user-images.githubusercontent.com/113898917/204310903-2261c379-f474-4d42-b761-05c9bad5fe8b.png)
![XOR7](https://user-images.githubusercontent.com/113898917/204310911-3d4b65e3-b909-4391-90d9-ca5d6dd492b5.png)
![XOR9](https://user-images.githubusercontent.com/113898917/204310920-982db6be-4072-4dcd-bd3f-9c699879ceb3.png)


## Задание 2
### Построить график с анализом кол-ва ошибок у каждой операции:                                                                           
   ![Графики кол-ва ошибок](https://user-images.githubusercontent.com/113898917/204315273-7691b0b9-6441-4917-9145-58b32387f3e3.png)

## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity:
   Для визуальной модели я выбрал операцию XOR, так как она показалась мне самой интересной, для этого я воспользовался таким свойством объектов как триггер:
   так, когда один кубик падает на другой, он меняет свой цвет в зависимости от цвета другого куба:
      
      using System.Collections;     
      using System.Collections.Generic;
      using UnityEngine;
      public class PerceptronParody : MonoBehaviour
      {
          private void OnTriggerEnter(Collider other)
          {
              if (other.gameObject.GetComponent<Renderer>().material.color == Color.green && this.gameObject.GetComponent<Renderer>().material.color == Color.magenta)
              {
                  other.gameObject.GetComponent<Renderer>().material.color = Color.magenta;
                  this.gameObject.GetComponent<Renderer>().material.color = Color.magenta;
              }
              else if (other.gameObject.GetComponent<Renderer>().material.color == Color.magenta && this.gameObject.GetComponent<Renderer>().material.color == Color.green)
              {
                  other.gameObject.GetComponent<Renderer>().material.color = Color.magenta;
                  this.gameObject.GetComponent<Renderer>().material.color = Color.magenta;
              }
              else
              {
                  other.gameObject.GetComponent<Renderer>().material.color = Color.green;
                  this.gameObject.GetComponent<Renderer>().material.color = Color.green;
              }
          }
      }
 

   
 

https://user-images.githubusercontent.com/113898917/204329381-aa926fc5-2a7f-4f90-8ac6-06671b0bb4c7.mp4

Данный код можно адаптировать/менять под другие операции, достаточно лишь поменять цвет в условиях.

## Выводы
   1. Узнал что такое перцептрон и для чего его используют.
   2. Попытался создать свой и посмотреть как он работает в условиях разных логических операциях (как он им "учится").
   3. Проанализировал кол-во ошибок и итерации при работе перцептрона и создал на основе этого соответствующие графики.
   4. Попробовал визуализировать работу перцептрона при заданной операции XOR.
