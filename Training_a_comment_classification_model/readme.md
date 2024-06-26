# Обучение модели классификации комментариев

### Задача
Интернет-магазин запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Требуется инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

Нужно обучить модель классифицировать комментарии на позитивные и негативные. В нашем распоряжении набор данных с разметкой о токсичности правок.

Нужно построить модель со значением метрики качества *F1* не меньше 0.75. 
   
## Этапы исследования
**1. Подготовка данных.**

    1.1.  Загрузка данных.
    1.2. Лемматизация текста.
    1.3. Устранение стоп-слов.

**2. Обучение.**

    2.1. Логистическая регрессия.
    2.2. LightGBM.

**3. Выводы.**
    
## Выводы
В ходе исследования была проделана следующая работа:
1. Подготовка данных:
- Данные были проверены на наличие пропусков и дубликатов. Их не было обнаружено.
- В данных присутствует сильный дисбаланс классов: прмеров с классом 0 - 90%, а с классом 1 - 10%.
- Мы провели лемматизацию текста, сохранив результаты в промежуточный файл.
- Очистили данные от стоп-слов.
- Провели TF-IDF преобразование, с ограничением в 15 000 признаков.
2. Обучение модели:
- Мы обучили модель логической регресии, и с помощью GridSearchCV подобрали лучшие гиперпараметры: C = 10, class_weight = None. На кросс-валидации модель показала значение f1-меры равное 0.77.
3. Тестироввание модели:
- На тестовой выборке модель показала значение f1-меры равное 0.78.

Итак, нам удалось достичь значение f1-меры более 0.75.
