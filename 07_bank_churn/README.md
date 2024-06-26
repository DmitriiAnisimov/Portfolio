# Прогнозирование оттока клиента Банка

## Описание проекта
В данном проекте проводится анализ данных для прогнозирования оттока клиентов банка. Из банка начали уходить клиенты каждый месяц, и банковские маркетологи решили разработать модель для прогнозирования ухода клиентов. На основе исторических данных о поведении клиентов и расторжении договоров с банком строится модель, которая определяет клиентов, склонных к оттоку.

## Навыки и инструменты
- Matplotlib
- Pandas
- Scikit-learn

## Задачи проекта
1. Провести анализ и предобработку данных.
2. Построить модель для прогнозирования оттока клиентов.
3. Оценить качество модели и её предсказательные способности.

## Вывод

1. Проведена подготовка данных. попущенные значения были заполнены медианой, так как пропусков 9% и при удалении пропусков, модели на валидации показывалии худшее значение метрики f1.
2. Исследован дисбаланс классов. Объектов класса 1 - 20% от выборки.
3. Подготовлены признаки для обучения модели. Переведены из строковых к числовым.
4. Применены методы борьбы с дисбалансом. Лучше всего себя паказал метод взвешивания классов.
6. Результат тестирования выбранной модели: f1 - `0.64` и roc-auc - `0.87`.
