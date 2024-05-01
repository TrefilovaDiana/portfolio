## Определение выгодного тарифа для телеком компании

### Задача
На основе данных клиентов оператора сотовой связи проанализировать поведение клиентов и поиск оптимального тарифа.
   
## Этапы исследования
**1. Проведение обзора данных.**

**2. Проведение предобработки данных.**
- Привести столбцы reg_date из таблицы users, churn_date из таблицы users, call_date из таблицы calls,message_date из таблицы messages и session_date из таблицы sessions к новому типу с помощью метода to_datetime();
- Привести столбец duration из таблицы calls к типу int;
- Удалить столбец Unnamed: 0 из датафрейма sessions;
- Создать столбцы month с номером месяца в датафреймах calls, messages и sessions;
- Посчитать количество звонков для каждого пользователя по месяцам;
- Посчитать количество израсходованных минут разговора для каждого пользователя по месяцам;
- Псчитать количество отправленных сообщений по месяцам для каждого пользователя;
- Посчитать количество потраченных мегабайт по месяцам для каждого пользователя.

**3. Проанализировать данные и подсчитать выручку.**

**4. Проверка гипотез.**
- Средняя выручка пользователей тарифов «Ультра» и «Смарт» различается;
- Средняя выручка с пользователей из Москвы отличается от выручки c пользователей других регионов.

**5. Выводы.**

## Выводы
В ходе ииследования мы выяснили, что:
- Средняя длительность разговоров у абонентов тарифа Ultra больше, чем у абонентов тарифа Smart. В течение года пользователи обоих тарифов увеличивают среднюю продолжительность своих разговоров. Рост средней длительности разговоров у абонентов тарифа Smart равномерный в течение года. Пользователи тарифа Ultra не проявляют подобной линейной стабильности. Стоит отметить, что феврале у абонентов обоих тарифных планов наблюдались самые низкие показатели.
- В среднем пользователи тарифа Ultra отправляют больше сообщений — почти на 20 сообщений больше, чем пользователи тарифа Smart. Количество сообщений в течение года на обоих тарифах растёт. Динамика по отправке сообщений схожа с тенденциями по длительности разговоров: в феврале отмечено наименьшее количество сообщений за год и пользователи тарифа Ultra также проявляют нелинейную положительную динамику.
- Меньше всего пользователи использовали интернет в январе, феврале и апреле. Чаще всего абоненты тарифа Smart тратят 15–17 Гб, а абоненты тарифного плана Ultra — 19–21 ГБ.