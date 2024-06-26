# Разработка системы предупреждения аварий на каршеринге

## Описание проекта
Данный проект посвящен разработке системы предупреждения аварий на каршеринге на основе исторических данных из базы данных. Целью проекта является выявление причин возникновения аварий и создание алерта о безопасном вождении для клиентов каршеринга.

## Навыки и инструменты
- Pandas
- PostgreSQL
- SQL
- SQLAlchemy
- Scikit-learn

## Задачи проекта
1. Импорт и предварительный анализ исторических данных из базы данных каршеринга.
2. Подготовка данных для анализа причин возникновения аварий.
3. Исследовательский анализ данных для выявления основных факторов, влияющих на аварийность.
4. Построение модели предупреждения аварий на основе машинного обучения.
5. Создание алерта о безопасном вождении для клиентов каршеринга на основе результатов анализа данных и моделирования.

## Вывод
Нам удалось обучить модель на тестовых данных и получить метрику Recall равную 64%, precision - 71%.


Мы увидели что самыми влияющими факторами являются (если отсеять одинаковые для всех сторон факторы):

* `collision_time` (время ДТП),
* `insurance_premium` (страховая премия), 
* `vehicle_age` (возраст авто), 
* `collision_date`(день недели),
* `direction0`(направление). 

Ночная езда (c 12 ночи до 5 утра) более опасна, чем дневная. Ночью вероятность ошибки у водителя выше.

Я добавил бы следующие характеристики клиента:
* возраст водителя, который будет прямо влиять на время реакции,
* водительский стаж,
* количество нарушений.
