###Базовые переменные и определения

`@api_url` - https://admin.docent.uz/api


`@api_url_v1` - https://admin.docent.uz/api/v1

`@GET|@POST|@POST|@PUT` - глаголы запроса

`@RESP` - возвращаемый ответ


`some_url[@somevalue]` - необязательный параметр `@somevalue` в запросе

`some_url{@somevalue}` - обязательный параметр `@somevalue` в запросе

`@pagination` - cтруктура ответа пагинации, имеет следующий вид
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

###Разделы

[Авторизация](./auth/index.md)

[Письма](./messages/index.md)

[Документы](./documents/index.md)

[Задачи](./tasks/index.md)


