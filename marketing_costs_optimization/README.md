# Оптимизация марĸетинговых затрат в Яндеĸс.Афише

# Исследовательская задача:
предложить оптимизацию маркетинговых затрат.

# Краткое описание структуры проекта:
1. Проведена предобработка данных (проверка на пропуски, логику, корректность форматов данных)
2. Построение отчётов и расчёт метрик Здесь произведен когортный анализ, затронуты такие вопросы, как:
- сколько людей пользуется продуктом (DAU, WAU, MAU), сколько сессий и их длительность, retention(как часто люди возвращаются);
- когда начинают покупать, сколько покупают и какой средний чек, сколько приносят денег (LTV);
- сколько денег было потрачено на маркетинг, сколько стоило привлечение одного клиента (CAC), на сколько окупились расходы (ROI).
3. Даны рекомендации по самым перспективным и прибыльным источникам рекламы.


В распоряжении следующие данные:
* лог сервера с данными о посещениях сайта Яндекс.Афиши,
* выгрузка всех заказов за этот период,
* статистика рекламных расходов.

# Описание данных:

**Таблица visits (лог сервера с информацией о посещениях сайта):**
- Uid — уникальный идентификатор пользователя
- Device — категория устройства пользователя
- Start Ts — дата и время начала сессии
- End Ts — дата и время окончания сессии
- Source Id — идентификатор рекламного источника, из которого пришел пользователь

**Таблица orders (информация о заказах):**
- Uid — уникальный id пользователя, который сделал заказ
- Buy Ts — дата и время заказа
- Revenue — выручка Яндекс.Афиши с этого заказа


**Таблица costs (информация о затратах на маркетинг):**
- source_id — идентификатор рекламного источника
- dt — дата
- costs — затраты на этот рекламный источник в этот день

# Используемые в проекте библиотеки
pandas, matplotlib, seaborn, numpy
