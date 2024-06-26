# Обработка фотографий покупателя

## Описание проекта
В данном проекте разрабатывается система компьютерного зрения для обработки фотографий покупателей в сетевом супермаркете. Фотофиксация в прикассовой зоне позволит определять возраст клиентов для анализа их покупок, предложения товаров, соответствующих их возрастной группе, а также контроля добросовестности кассиров при продаже алкоголя. Строится модель, которая по фотографии определит приблизительный возраст человека. В распоряжении имеется набор фотографий людей с указанием их возраста.

## Навыки и инструменты
- Keras
- Python

## Задачи проекта
1. Загрузка и анализ набора фотографий покупателей.
2. Подготовка данных для обучения модели.
3. Обучение модели на фотографиях для определения возраста.
4. Оценка качества модели и ее настройка.
5. Разработка инструмента для определения возраста на фотографиях.

## Вывод
Построенная модель по фото определяет возраст с ошибкой примерно 7 лет.

Если использовать эту модель, то ее достаточно для решения первой задачи - анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы. И лучше, если покупателей разбивать на группы, например, с шагом 10.

Но для решения второй задачи - решение о продаже алкоголя - качества модели недостаточно. Если человеку 24 года, модель может определить его как 17-летнего и "запретить" продажу алкоголя. И тогда магазин лишится прибыли. Поэтому тут в спорных случаях можно подключить распознавание паспорта / водительского удостоверения.
