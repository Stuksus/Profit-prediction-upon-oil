#<h1>Содержание<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Прогнозирование-оттока-клиентов-банка" data-toc-modified-id="Прогнозирование-оттока-клиентов-банка-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Прогнозирование оттока клиентов банка</a></span><ul class="toc-item"><li><span><a href="#Описание-проекта" data-toc-modified-id="Описание-проекта-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Описание проекта</a></span></li><li><span><a href="#Описание-данных" data-toc-modified-id="Описание-данных-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Описание данных</a></span></li><li><span><a href="#Вывод" data-toc-modified-id="Вывод-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Вывод</a></span></li></ul></li><li><span><a href="#Прогнозирование-прибыли-от-нефтяной-скважины" data-toc-modified-id="Прогнозирование-прибыли-от-нефтяной-скважины-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Прогнозирование прибыли от нефтяной скважины</a></span><ul class="toc-item"><li><span><a href="#Описание-проекта" data-toc-modified-id="Описание-проекта-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Описание проекта</a></span></li><li><span><a href="#Условия-задачи:" data-toc-modified-id="Условия-задачи:-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Условия задачи:</a></span></li><li><span><a href="#Вывод" data-toc-modified-id="Вывод-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Вывод</a></span></li></ul></li></ul></div>

# Прогнозирование прибыли от нефтяной скважины
## Описание проекта
Нужно решить, где бурить новую скважину.
Шаги для выбора локации обычно такие:
- В избранном регионе собирают характеристики для скважин: качество нефти и объём её запасов;
- Строят модель для предсказания объёма запасов в новых скважинах;
- Выбирают скважины с самыми высокими оценками значений;
- Определяют регион с максимальной суммарной прибылью отобранных скважин.
Мне предоставлены пробы нефти в трёх регионах. Характеристики для каждой скважины в регионе уже известны. Необходимо построить модель для определения региона, где добыча принесёт наибольшую прибыль.

## Условия задачи:
- Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).
- При разведке региона исследуют 500 точек, из которых с помощью машинного обучения выбирают 200 лучших для разработки.
- Бюджет на разработку скважин в регионе — 10 млрд рублей.
- При нынешних ценах один баррель сырья приносит 450 рублей дохода. Доход с каждой единицы продукта составляет 450 тыс. рублей, поскольку объём указан в тысячах баррелей.
- После оценки рисков нужно оставить лишь те регионы, в которых вероятность убытков меньше 2.5%. Среди них выбирают регион с наибольшей средней прибылью.

## Вывод

- Нулевой регион:
    - Доверительный интервал: (-110 929 096.14, 891 087 236.3)
    - Точка безубыточности: 111.(1)
    - Средняя прибыль в нулевом регионе: 381 840 608.64
    - Риски: 6.7 %
- Второй регион: 
    - Доверительный интервал: (-142 559 672.52, 900 660 974.77)
    - Точка безубыточности: 111.(1)
    - Средняя прибыль с одной скважины во втором регионе: 382 973 380.22
    - Риски: 7 %
        
по условию рисков не подходит ни один из регионов. Если же выбирать из наименее рискованных, то наиболее подходящим будет нулевой регион. Но также можно заметить, что по сравнению со вторым регионом у него средняя прибыль меньше, в тоже время у второго региона на 0,3% выше риски.      



