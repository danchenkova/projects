
# Прогнозирование оттока клиентов

В связи с увеличившимся оттоком клиентов банка требуется подготовить модель с предельно большим значением F1-меры (минимальное значение метрики - от 0.59), оценивающую риски ухода того или иного клиента. Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

## Цель проекта
Построить наилучшую модель для прогнозирования, уйдет ли из банка клиент, основываясь на его характеристиках и статистике поведения.

## Задачи

1.	Изучить исходный датасет и общую статистику поведения клиентов.
2.	Подготовить данные для анализа, обработать признаки, разделить на обучающую, валидационную и тестовую выборки.
3.	Исследовать базовые модели и рассмотреть, как меняются показатели оценки в зависимости от примененной модели. Подобрать гиперпараметры.
4.	Выбрать наилучшую модель, по-возможности доработать ее, учитывая дисбаланс классов.
5.	Проверить модели на тестовой выборке и подготовить рекомендации.

В проекте по сути рассмотрена задача бинарной классификации. Классы не сбалансированы, в предоставленном датасете есть существенная диспропорция в размерах категорий. Примерное соотношение текущих и бывших клиентов - 4:1. 

Между возрастом, балансом на счете и вероятностью оттока выявлена небольшая положительная корреляция. А вот между активностью клиента и количеством используемых продуктов вероятность «исхода»  коррелирует отрицательно, хоть эта связь и незначительна.

В проекте рассмотрено пять моделей: дерево решений, случайный лес, логистическая регрессия, наивный байесовский классификатор и метод опорных векторов, оптимальные гиперпараметры подбирались с помощью функции GridSearchCV(). Также применено несколько способов решения проблемы дисбаланса классов: взвешивание, уменьшение и увеличение выборки.

Лучший итог показал взвешенный Random Forest, f1-score = 0.618 на валидационной выборке и столько же на тестовой. Отметим, что это единственная модель, у которой recall и precision примерно равны. Также озвученный порог (f1-score >= 0.59) преодолели еще три модели: случайные леса, обученные на сбалансированной увеличенной выборке (0.619 и 0.613), уменьшенной выборке(0.603 и 0.595) и взвешенный метод опорных векторов (0.611 и 0.594). 

Используемые библиотеки: pandas, numpy, matplotlib, scikit-learn.