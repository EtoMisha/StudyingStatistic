# PeerStat (beta)
## Сервис статистики для студентов Школы 21

https://21world.ddns.net/

Приложение парсит учебную платформу Школы, собирает разные данные о студентах и выводит в виде удобной таблицы с фильтрами и сортировкой.

Обновляется раз в сутки, для получения токена логинится с помощью Selenium (костыль конечно, но нормального API для авторизации там нет).

Данные собираются через запросы к graphQL сервису учебной платформы, но так как доступа к graphQL Schema тоже нет, приходится формировать тело запроса вручную в виде json с подстановкой значения переменных.
