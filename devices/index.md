<h4>Управление устройствами пользователя</h4>

Пользователь может авторизовать свои устройства в системе.
Устройству привязывается Firebase Token и дублируются 
event ы в этот канал (e.g. `NewMessage`, `NewTask`, `DocumentResoluted`)


Список устройств пользователя:
```
@throttle 5, 1
@GET      @api_url_v1/devices
@RESP     @collection
```

Авторизация нового устройства:
```
@throttle 5, 1
@POST     @api_url_v1/devices
@DATA     {
             String name   - Название устройства (можно модель,например: Artel P5)
             String token  - Firebase Token 
          }

@RESP     @record
```

Удаление устройства из базы:

```
@throttle 5, 1
@DELETE   @api_url_v1/devices/{id}
@RESP     @record
```
где `@id` - Docent ID устройства

<h4>Примеры:</h4>

Добавление нового устройства

`POST api_url_v1/devices`

`{"name":"My Phone", "token":"ad12nen12neadnui2n3"}`




[back](..)