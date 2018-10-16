Для получения все изменения в письмах пользователя надо 
обращаться по адресу


```
GET  api_url/messages/{@type}/updated[?@params]
RESP @pagination
```
где 

`@type`

значение | описание 
---|---
inbox | полученные 
sent | отправленные 
reports | отчеты (в разработке) 

`@params` 

ключ | тип | описание 
---|---|---
from | DateTime |минимальная дата обновления, формат `Y-m-d H:i:s`

####Ответ
`@pagination`


####Примеры
+ все обновления в почте в разделе входящие

`GET api_url/messages/inbox/updated`



+ все обновления в почте в разделе исходящие после 10 ого cентября

`GET api_url/messages/inbox/updated?from=2010-09-10 10:32:21`
