# Построение модели определения стоимости автомобиля

### Задача
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. В нашем распоряжении исторические данные: технические характеристики, комплектации и цены автомобилей. Нам нужно построить модель для определения стоимости. 

Заказчику важны:

- качество предсказания;
- скорость предсказания;
- время обучения.
   
## Этапы исследования
**1. Подготовка данных.**

**2. Обучение моделей.**

**3. Анализ моделей.**

**4. Выводы.**

## Выводы
В ходе работы были выполнены следующие этапы:
1. Предобработка и анализ данных:
- исправлены названия столбцов;
- обработаны пропуски;
- устранены аномальные значения;
- для модели выбраны только те количественные признаки, которые имеют значимую корреляцию с целевым признаком. Также мы избавились от ненужных категориальных признаков.
2. Пострение моделей:
- Данные были разделены на обучающую и тестовую выборки;
- проведено масштабирование и кодирование данных;
- построена линейная модель, которая показала rmse - 2878.3, время обучения - 52.9 s, время предсказания: 91.5 ms;
- построена модель случайного леса, которая показала rmse - 2097.14, время обучения - 23min 33s, время предсказания: 6.82 s;
- построена модель градиентного бустинга, которая показала rmse - 2409.5, время обучения:  5.69 s, время предсказания - 2.73 s;
- также была проверена константная модель, которая показала rmse - 4959.8, время обучения: 3.16 ms, время предсказания - 661 µs.
3. Выбор модели:
- В соответствии с требованиями заказчика, мы рекомендуем выбрать модель градиентного бустинга.
4. проверка модели градиентного бустинга на тестовой выборке:
- на тестовой выборке модель градиентного бустинга показала rmse - 2373.2.
