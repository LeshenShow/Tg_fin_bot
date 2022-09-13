# Tg_fin_bot

## Установка программы:
```
Скачивание с git: $ git clone https://github.com/LeshenShow/TG_fin_bot.git
Установка библиотек: pip install -r requirements.txt
config/my_token.txt = 'TOKEN'
Обновление базы данных: $ python sql_stock_bd.py
Запуск: $ python main.py
```
## Возможности бота:
### 1. Конвертация валют с сайта МосБиржи, либо Yahoo, если сервер не ответит.
```
Пример: пишем в следующем виде без кавычек '$', '10$', '322.58$' и т.д. получим курс $ помноженный на значение.

Отправляем 10$ Получаем 607.52 руб. 

Аналогично работает и с "€", и  с "¥"(китайский юань), данные предоставляются МосБиржей и Yahoo.
```

### 2. Получение котировок акций с МосБиржи и американских бирж (NYSE, Nasdaq и т.д.) в формате:
```
Цена акции, капитализация в млрд., изменение за день с открытия торгов в %, поставщик услуг.

Пример: отправляем AAPL или SBER (или !AAPL, !SBER) - получаем сообщение с показателями и наименованием информатора.

Для иностранных акций доступен график за год + сравнение с индексом S&P 500.

Для всех акций доступно получение более широкого списка показателей P/E, P/B, Sector и т.д. от Yahoo.

P.S. Для групповых чатов запрос доступен ТОЛЬКО через "!" (!GAZP), при этом дополнительные опции отключены.
```
### 3. Получение информации по индексам МосБиржи "IMOEX", S&P 500.
```
Для получения данных по S&P нужен запрос 'snp' или 's&p' (или ^GSPC).

Для индексов доступны те же режимы, что и для акций. 

    Дополнительно для индекса МосБиржи есть такие опции:
* Получение списка топ 10 акций в составе индекса с доп. информацией: долей в индексе и т.д.
* Получение остального списка (№10 и до окончания) с доп. информацией.
* Круговая диаграмма списка топ 10 для наглядного представления распределения активов.
* Гистограмма остального  списка.

P.S. запрос через Yahoo может составлять 5-6 секунд, это нормально.

Вопросы, предложения: @leshen_also

Поставщики информации:

MOEX:   https://www.moex.com/

Yahoo:  https://finance.yahoo.com/

Eninvs: https://eninvs.com/

Внимание! с августа 2022 Yahoo отключил поставку данных для российских инструментов, связи с чем могут быть ненадежные 
данные по расширенным показателям акций/ индексов из России.
```
