
# Определение перспективного тарифа для оператора сотовой связи

Оператор сотовой связи предлагает два тарифных плана: Smart и Ultra. Необходимо разобраться, какой тариф приносит больший доход и является наиболее перспективным с точки зрения продвижения среди потенциальных клиентов. С этой целью компания предоставила для анализа небольшую выборку клиентов (500 человек).

## Цель проекта

Исследовать по выборочным данным поведение клиентов телекоммуникационной компании и выявить наиболее перспективный тариф с точки зрения получения прибыли, привлечения новых клиентов и удержания настоящих.

## Задачи проекта

1. Изучить исходные датасеты на предмет корректного типа данных, отсутствующих значений и наличия дубликатов.
2. Рассчитать необходимые для дальнейшего анализа параметры.
3. Изучить общую статистику по звонкам, сообщениям и интернет-трафику.
4. Сформулировать гипотезы о доходности тарифов и провести проверку этих гипотез.

Для анализа данных предоставлено 5 таблиц, каждая из которых содержит свой фрагмент общей картины: информация по пользователям, совершенным звонкам, посланным сообщениям, объеме использованного сетевого трафика и общая справка о тарифах.
Для удобства работы с данными осуществлен ряд объединений таблиц, чтобы связать статистику по действиям пользователей (звонки, сообщения, интернет-соединения) с названиями тарифов и городов. 

Рассчитаны дополнительные параметры по каждому пользователю, необходимые для дальнейшего анализа (средняя длительность звонков в месяц, среднее количество посланных сообщений и средний ежемесячный объем использованного сетевого трафика). Далее, исходя из этих величин и условий тарифов, установлена средняя ежемесячная выручка с каждого абонента.

С точки зрения доходности с одного клиента более прибыльным тарифом является Ultra, но по доле в общей выручке большую выгоду приносит Smart (0,4 и 0,6 соответственно). 

В исследовании проверены две гипотезы о том, что средняя выручка абонентов тарифов Ultra и Smart не имеет значимых отличий, и что средняя выручка пользователей из Москвы не отличается от выручки пользователей из других регионов.
В первом случае расчеты выявили, что, скорее всего, верно обратное, и тарифы по своей выручке с одного абонента не похожи друг на друга.
Во втором нулевая гипотеза отвергнута не была. Клиенты тратят одинаковое количество денег на услуги связи вне зависимости от места проживания. 

Используемые библиотеки: scipy, numpy, pandas, matplotlib.
