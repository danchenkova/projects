
# Изучение рынка компьютерных игр

Для определения популярных продуктов, оценки их потенциала и планирования рекламных кампаний, интернет-магазину необходимо провести исследование по компьютерным играм. Анализ проводится на основе исторических данных о продажах игр, оценок пользователей и экспертов, доступных в открытых источниках. В датасете перечислены игры, выходившие до 2016 года. 

## Цель проекта
Выявить факторы, определяющие успешность игры и, возможно, способствующие высоким продажам.

## Задачи

1.	Изучить исходный датасет на предмет корректного типа данных, отсутствующих значений, наличия дубликатов и прочих несоответствий.
2.	Обработать данные там, где это необходимо, и рассчитать нужные для дальнейшего анализа параметры.
3.	Изучить общую статистику по продажам игр в разрезах по годам, платформам и жанрам.
4.	Рассмотреть, как меняется портрет пользователя в зависимости от региона.
5.	Сформулировать гипотезы о пользовательских рейтингах платформ и жанров и провести проверку этих гипотез.

В проекте проведена работа с подготовкой данных к анализу: убраны пропущенные значения, ряд столбцов приведен к корректному типу, обработаны аномальные значения.

По статистике продаж за 2016 год определены наиболее перспективные игры в разрезе платформ. Ими оказались продукты для PS4, XOne и 3DS.
Выявлена зависимость между уровнем продаж и оценками критиков. Выведен список и самых продаваемых жанров по регионам.

Гипотеза о равенстве средних пользовательских рейтингов платформ Xbox One и PC была принята, а вот о равенстве средних пользовательских рейтингов жанров Action и Sports отвергнута. 

Используемые библиотеки: scipy, numpy, pandas, matplotlib.
