<h3>Базовые переменные и определения</h3>

<h4>Обозначения по запросам</h4>

`@api_url` - https://admin.docent.uz/api

`@api_url_v1` - https://admin.docent.uz/api/v1

`@GET|@POST|@POST|@PUT` - глаголы запроса

`some_url[@somevalue]` - необязательный параметр `@somevalue` в запросе

`some_url{@somevalue}` - обязательный параметр `@somevalue` в запросе

`@throttle limit, minutes` - ограничения по количеству запросов в минуту по url-у. Например, `@throttle 5, 1` - максимум 5 запросов в минуту по url-у

`@DATA` - тело запроса. например, 
```json
{
  String name,
  Number age,
}
```
соответствует данным {"name": "coder", "age": 29}

<h4>Обозначения по респонсам</h4>

`@RESP` - возвращаемый ответ

`@record` - Одна сущность
```json
{
  "name": "docent",
  "version": "0.1.2-dev",
  "author": "standart it sektor"
}
```

`@collection` - коллекция записей ввиде массива
```json
[{"name": "doc"}, {"name": "ent"}]
```


`@pagination` - ответа в виде пагинации, имеет следующую структуру:
```json
{
  "current_page": 1,
  "data": [],
  "from":1,
  "last_page":1,
  "next_page_url":null,
  "path":"somelink",
  "per_page":10,
  "prev_page_url":null,
  "to":1,
  "total":1
  }
```

<h3>Разделы</h3>

[Авторизация](./auth/index.md)

[Письма](./messages/index.md)

[Документы](./documents/index.md)

[Задачи](./tasks/index.md)

[Устройства](./devices/index.md)


