# PeerStat (beta)
## Сервис статистики для студентов Школы 21

https://21world.ru/stat

Приложение парсит учебную платформу Школы, собирает разные данные о студентах и выводит в виде удобной таблицы с фильтрами и сортировкой.

Обновляется раз в сутки, для получения токена логинится с помощью Selenium (костыль конечно, но нормального API для авторизации там нет).

Данные собираются через запросы к graphQL сервису учебной платформы, но так как доступа к graphQL Schema тоже нет, приходится формировать тело запроса вручную в виде json с подстановкой значения переменных.

Таблица с данными генерируется на стороне сервера с помощью Thymeleaf шаблона, на фронте для фильтров, сортировки и пагинации используется библиотека datatable (https://github.com/Holt59/datatable)

### WIP

to do:
- добавить страницу с данными по проектам
- вынести парсер в отдельный модуль
- завернуть всё в docker compose