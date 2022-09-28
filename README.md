# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил:
- Волков Кирилл Дмитриевич
- РИ210914
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
- Код реализации выполнения задания. Визуализация результатов выполнения.
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения.
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения.
- Выводы.

## Цель работы
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1

- Скриншоты выполнения скрипта в google.colab и сохранения его на гугл диск:
 <img width="1904" alt="Снимок экрана 2022-09-28 в 14 34 12" src="https://user-images.githubusercontent.com/79734984/192783142-bad66b05-6ef1-4b01-858f-b50c78b9f222.png">
 <img width="1904" alt="Снимок экрана 2022-09-28 в 14 35 05" src="https://user-images.githubusercontent.com/79734984/192783144-fd9ed3f6-4097-4a42-b2fe-78b88d132360.png">

- Hello World в Unity:
 <img width="1904" alt="Снимок экрана 2022-09-27 в 19 57 29" src="https://user-images.githubusercontent.com/79734984/192783656-3c64643e-04fa-422c-8d5b-12cdde6ad252.png">



## Задание 2

- Подготовка данных для алгоритма линейной регрессии

![Снимок экрана 2022-09-28 в 14 55 10](https://user-images.githubusercontent.com/79734984/192807705-30de43ac-b8b1-45a3-841d-4be933b62167.png)

- Определение функций модели, потери и оптимизации

<img width="1771" alt="Снимок экрана 2022-09-28 в 17 59 52" src="https://user-images.githubusercontent.com/79734984/192785153-30372d83-6d1f-4adb-ad8d-e218afb33fea.png">

- Инициализация гиперпараметров модели и 1 итерация

![Снимок экрана 2022-09-28 в 18 03 11](https://user-images.githubusercontent.com/79734984/192786677-c979098f-318a-4c7a-94f4-90d49f6124f3.png)

- 2 итерации

![Снимок экрана 2022-09-28 в 18 03 50](https://user-images.githubusercontent.com/79734984/192786870-26f20e6f-01e3-4940-b8c7-24f369820acc.png)

- 3 итерации

![Снимок экрана 2022-09-28 в 18 04 14](https://user-images.githubusercontent.com/79734984/192786918-5772e510-3fee-4755-b0b6-bb6904d4424c.png)

- 4 итерации

![Снимок экрана 2022-09-28 в 18 04 26](https://user-images.githubusercontent.com/79734984/192786957-ce232010-dfbb-4c5c-87a2-2a29d10c82a5.png)

- 5 итераций

![Снимок экрана 2022-09-28 в 18 04 37](https://user-images.githubusercontent.com/79734984/192786981-e6b6cc8e-11af-445b-9985-a04bedccccbf.png)

- 10000 итераций

![Снимок экрана 2022-09-28 в 18 06 06](https://user-images.githubusercontent.com/79734984/192787032-b0aaf3be-1bdf-4b58-af39-6469f15e4e1c.png)

Код задания находится в [этом репозитории](https://github.com/caimanchik/firstLab/blob/main/program.ipynb)


## Задание 3

### Должна ли величина loss стремиться к нулю при изменении исходных данных?

- Прежде всего надо сказать, что loss - среднеквадратичное отклонение(ошибка). Величина loss может стремиться к нулю при изменении исходных данных. Чтобы показать это, я присвоил переменной ```y``` значение переменной ```x```, домноженное на коэффициент 2.

![Снимок экрана 2022-09-28 в 16 46 55](https://user-images.githubusercontent.com/79734984/192788708-21315670-ed80-401e-b6d2-84caa2f36d1d.png)

- Полученный результат через 10000 итераций:

![Снимок экрана 2022-09-28 в 16 47 09](https://user-images.githubusercontent.com/79734984/192788849-a0854c10-e57e-4949-81f6-045d6269d777.png)

### Какова роль параметра Lr?

- Параметр Lr можно расшифровать как learning rate, в переводе на русский - скорость обучения. Меняя этот параметр, мы как бы меняем скорость изменения весов(насколько я это понял). Особенно это заметно на небольшом количестве итераций. В качестве примера я взял модель из Задания1 с теми же исходными данными

![Снимок экрана 2022-09-28 в 18 32 02](https://user-images.githubusercontent.com/79734984/192792233-a4e83439-c701-4fb0-847d-56c9c89965db.png)
![Снимок экрана 2022-09-28 в 18 32 44](https://user-images.githubusercontent.com/79734984/192792239-c26b98c8-4c7a-4f5a-affe-eb264a177c6c.png)

На первом скриншоте среднеквадратичное отклонение больше, чем на втором, потому что длина шага оказалась слишком мала, чтобы функция оптимизации успела отработать корректно. 


## Выводы

В данной лабораторной работе я познакомился с интерфейсом google.colab и Unity. Также я изучил алгоритм линейной регрессии

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
