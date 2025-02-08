# Кейс – Мобильные игры

В этом проекте были рассмотрены различные аспекты мобильного приложения компании, занимающейся разработкой мобильных игр.

Анализ проводился с использованием *Python* и *Jupyter Notebook*.

---

## Задача 1

**Retention** – один из ключевых показателей в компании. Вам необходимо разработать функцию, рассчитывающую удержание игроков (по дням с момента их регистрации). Данные хранятся в папке *shared* и имеют следующую структуру:

- `shared/problem1-reg_data.csv` – информация о времени регистрации:

| reg_ts | uid |
|--------|-----|
| 906166566 | 2 |
| 906344325 | 2 |
| 906686169 | 2 |
| 906893386 | 2 |
| 906980227 | 2 |

- `shared/problem1-auth_data.csv` – данные о времени входа пользователей в игру:

| auth_ts | uid |
|---------|-----|
| 906166566 | 2 |
| 924422172 | 3 |
| 937374732 | 4 |
| 947425117 | 5 |
| 955630339 | 6 |

---

## Задача 2

Проведен A/B-тест, в котором пользователям предлагались разные варианты акционных предложений. Установлено, что **ARPU** в тестовой группе выше на 5% по сравнению с контрольной. 

При этом:
- В контрольной группе 1928 из 202103 пользователей совершили покупки.
- В тестовой группе 1805 из 202667 игроков стали платящими.

**Вопросы для анализа:**
- Какой из вариантов предложений является наиболее эффективным?
- Какие метрики следует рассмотреть для корректного вывода?
- Каким образом провести анализ?

Пример данных:

| user_id | revenue | testgroup |
|---------|---------|----------|
| 1 | 0 | b |
| 2 | 0 | a |
| 3 | 0 | a |
| 4 | 0 | b |
| 5 | 0 | b |

---

## Задача 3

В игре *Plants & Gardens* ежемесячно проходят временные тематические события, в которых игроки могут получать эксклюзивные предметы, персонажей, бонусные монеты и другие награды. Для получения приза необходимо пройти определенное количество уровней в установленный срок.

**Анализ:**
- Какие метрики помогут оценить результаты последнего завершенного события?
- Как повлияет изменение механики, при котором игрок откатывается на несколько уровней назад после неудачной попытки? Нужно ли пересматривать набор метрик?

---

## Реализация проекта

- Проведен **разведочный анализ данных (EDA)** и их предобработка.
- Рассчитан **Retention** на тренировочном наборе данных.
- Разработана **функция для расчета Retention** пользователей.
- Использован **API** для загрузки данных.
- Вычислены и проанализированы ключевые продуктовые метрики (**Conversion Rate, ARPU, ARPPU, конверсия**).
- Проверены гипотезы и проведен анализ результатов **A/B-теста** с применением статистических методов (*Хи-квадрат, t-test*).
- Сделаны выводы на основе полученных данных.
- Определены метрики для оценки результатов последнего тематического события в игре *Plants & Gardens*. 
