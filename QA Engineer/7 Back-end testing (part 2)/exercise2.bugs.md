## Баг-репорты

## Activities

## Баг №1. Неверный код ответа при отправке запроса - Activities: создание новой активности (тело запроса корректно) код ответа 200

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Activities

Открыт эндпоинт POST​/api​/v1​/Activities

### Шаги:

Отправить запрос: POST​/api​/v1​/Activities

тело запроса:
```
 {
  "id": 31,
  "title": "Activity 31",
  "dueDate": "2023-06-14T14:46:44.2536687+00:00",
  "completed": true
 }
```
### ОЖ: 

- код ответа 201

- Тело ответа пустое

- Response headers:

access-control-allow-origin: *

api-supported-versions: 1.0

charset=utf-8; v=1.0

date: Mon12 Jun 2023 08:31:27 GMT

server: Kestrel

transfer-encoding: chunked

Location: https://fakerestapi.azurewebsites.net/api/v1/Activities

### ФР: 

- код ответа 200

- тело ответа:
```
{
  "id": 31,
  "title": "Activity 31",
  "dueDate": "2023-06-14T14:46:44.2536687+00:00",
  "completed": true
}
```
- заголовки ответа:

 access-control-allow-origin: * 
 
 api-supported-versions: 1.0 
 
 content-type: application/json; charset=utf-8; v=1.0 
 
 date: Tue13 Jun 2023 09:47:08 GMT 
 
 server: Kestrel 
 
 transfer-encoding: chunked 

### Серьезность: Blocker

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106



## Баг №2. Неверный код ответа при отправке запроса - Activities: создание новой активности (тело запроса некорректно) код ответа 400

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Activities

Открыт эндпоинт POST​/api​/v1​/Activities

### Шаги:

Отправить запрос: POST​/api​/v1​/Activities

тело запроса:
```
{
  "id": ,
  "title": "Activity 1",
  "dueDate": "2023-06-10T13:28:13.4432704+00:00",
  "completed":
}
```
### ОЖ: 

- код 409 Conflict

- Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
"error": "Activity with ID 1 already exists"
}
```
Поле JSON объекта соответствует аргументу метода сервиса

- Response headers:


api-supported-versions: 1.0 

content-type: application/json; charset=utf-8; v=1.0 

date: текущая дата и время по GMT 

server: Kestrel 

transfer-encoding: chunked

### ФР: 

код 400

тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-223ad5f1447c53428b467e7eac619f2c-d57b886a4a214f4b-00",
  "errors": {
    "$.id": [
      "',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 8."]
  }
}
```
- заголовки ответа:

 access-control-allow-origin: * 
 
 content-type: application/problem+json; charset=utf-8 
 
 date: Tue13 Jun 2023 09:53:57 GMT 
 
 server: Kestrel 
 
 
transfer-encoding: chunked 

### Серьезность: Critical

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №3. Неверный код ответа при отправке запроса - Activities: изменение активностей id и тело запроса некорректны (id=0, код 400)

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Activities

Открыт эндпоинт PUT​/api​/v1​/Activities​/{id}

### Шаги:

Отправить запрос: PUT​/api​/v1​/Activities​/0

тело запроса:
```
{
  "id": 0,
  "title": "Activity 2",
  "dueDate": "2023-06-10T13:28:13.4432704+00:00",
  "completed": 
}
```
### ОЖ: 

- код 404 Not Found

Тело ответа
```
{
"type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title": "Not Found",
"status": 404,
 "traceId": "`string`"
}
```
Response Headers


Content-Length: 0

Date: Sat, 10 Jun 2023 12:52:06 GMT

Server: Kestrel

### ФР: 

код 400

тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-9872ef38fdc56440bb5f827fbf14d7d2-4d89f3da0b60da47-00",
  "errors": {
    "$.completed": [
      "'}' is an invalid start of a value. Path: $.completed | LineNumber: 10 | BytePositionInLine: 0."
    ]
  }
}
```
- заголовки ответа:

 access-control-allow-origin: * 
 
 content-type: application/problem+json; charset=utf-8 
 
 date: Tue13 Jun 2023 10:05:52 GMT 
 
 server: Kestrel 
 
 transfer-encoding: chunked 

### ### Серьезность: Critical

Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №4. Неверный код ответа при отправке запроса - Activities:  удаление несуществующей активности id=0

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Activities

Открыт эндпоинт DELETE​/api​/v1​/Activities​/{id}

### Шаги:

Отправить запрос: DELETE​/api​/v1​/Activities​/0

### ОЖ: 

- код 404 Not Found

Тело ответа пустое

Response Headers

Content-Length: 0

Date: Sat, 10 Jun 2023 12:52:06 GMT

### ФР: 

код 200

тело ответа: пустое

- заголовки ответа:
 access-control-allow-origin: * 
 
 api-supported-versions: 1.0 
 
 content-length: 0 
 
 date: Tue13 Jun 2023 10:11:19 GMT 
 
 server: Kestrel

### Серьезность: Critical

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №5. Неверный код ответа при отправке запроса - Activities: получение информации о несуществующей активности id=" "пустой ввод

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Activities

Открыт эндпоинт GET​/api​/v1​/Activities​/{id}

### Шаги:

Отправить запрос: "GET​/api​/v1​/Activities​/ "

### ОЖ: 

- код 404 Not Found

Тело: 
```
{
"type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
"title": "Not Found",
"status": 404,
}
```
Response Headers

api-supported-versions: 1.0

content-type: application/problem+json; charset=utf-8; v=1.0

date: Mon12 Jun 2023 08:12:33 GMT

server: Kestrel

transfer-encoding: chunked

### ФР: 

Невозможно проверить отправку данного запроса и ответ на него в swagger 

### Серьезность: Blocker

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Authors

## Баг №6. Неверный код ответа при отправке запроса - Authors: создание нового авторов (тело запроса корректно) код ответа 200

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Authors

### Шаги:

Отправить запрос: POST​/api​/v1​/Authors

тело запроса:
```
{
  "id": 600,
  "idBook": 1,
  "firstName": "First Name 600",
  "lastName": "Last Name 600"
}
```
### ОЖ: 

- код 201

Тело: пустое

Response Headers

access-control-allow-origin: *

api-supported-versions: 1.0

content-type: application/json; charset=utf-8; v=1.0

date: Mon12 Jun 2023 08:41:15 GMT

server: Kestrel

transfer-encoding: chunked

Location: https://fakerestapi.azurewebsites.net/api​/v1​/Authors

### ФР: 

код ответа 200

Тело ответа: 
```
{
  "id": 600,
  "idBook": 1,
  "firstName": "First Name 600",
  "lastName": "Last Name 600"}
```
Структура ответа и заголовки:  access-control-allow-origin: * 
 api-supported-versions: 1.0 
 
 content-type: application/json; charset=utf-8; v=1.0 
 
 date: Tue13 Jun 2023 10:22:04 GMT 
 
 server: Kestrel 
 
 transfer-encoding: chunked 

### Серьезность: Blocker

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №7. Неверный код ответа при отправке запроса - Authors: создание нового авторов (тело запроса некорректно) код ответа 400

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Authors

### Шаги:

Отправить запрос: POST​/api​/v1​/Authors

тело запроса:
```
{
  "id": 600,
  "idBook": 1,
  "firstName": "First Name 600",
  "lastName":
}
```
### ОЖ: 

- код 409

Тело: 

Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{"error": "Authors with ID 600 already exists"}
```
Поле JSON объекта соответствует аргументу метода сервиса

Response Headers

api-supported-versions: 1.0 

content-type: application/json; charset=utf-8; v=1.0 

date: текущая дата и время по GMT 


server: Kestrel 

transfer-encoding: chunked

### ФР: 

код ответа 400

Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-54f328f3cf78af4fb8a2fd88938771f6-5f7ac6d3a7c3f246-00",
  "errors": {
    "$.lastName": [
    "'}' is an invalid start of a value. Path: $.lastName | LineNumber: 10 | BytePositionInLine: 0." ]}
```
заголовки:   

 access-control-allow-origin: * 
 
 content-type: application/problem+json; charset=utf-8 
 
 date: Tue13 Jun 2023 10:25:53 GMT 
 
 server: Kestrel 
 
 transfer-encoding: chunked 

### Серьезность: Critical

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №8. Неверный код ответа при отправке запроса - Authors: получение информации об авторах и книгах id=-1 некорректный - 200

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Authors

### Шаги:

Отправить запрос: GET​/api​/v1​/Authors​/authors​/books​/-1

### ОЖ: 

- код 400 Error: Bad Request

Тело: 
```
{ "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title": "One or more validation errors occurred.",
"status": 400,
"traceId": "00-d44d5c82380ac9439ad21f23c4acbedd-2968cee6eddcd84a-00",
"errors": {
"idBook": [
"The value '100000000000' is not valid."] }
```
Response Headers

charset=utf-8

date: Mon12 Jun 2023 08:46:27 GMT

server: Kestrel

ransfer-encoding: chunked

### ФР: 

код ответа 200

Тело ответа:
```
[]
```
заголовки:
api-supported-versions: 1.0 
 
 content-type: application/json; charset=utf-8; v=1.0 
 
 date: Tue13 Jun 2023 10:31:42 GMT 
 
 server: Kestrel 
 
 
 transfer-encoding: chunked

### Серьезность: Critical

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №9. Неверный код ответа при отправке запроса - Authors: получение информации об авторах и книгах id=" " пустой ввод (код 404)

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Authors

### Шаги:

Отправить запрос: «GET​/api​/v1​/Authors​/authors​/books​/ »

### ОЖ: 

- код 404 Not Found

Тело: 
```
{
"type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
"title": "Not Found",
"status": 404,
"traceId": "00-a33d0e01b2294145a4213b0accd48932-0da0aeedfd48dd49-00"
}
```
Response Headers


api-supported-versions: 1.0


charset=utf-8; v=1.0

date: Mon12 Jun 2023 08:53:40 GMT

server: Kestrel

transfer-encoding: chunked

### ФР:

Невозможно проверить отправку данного запроса и ответ на него в swagger 

### Серьезность: Blocker

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106


## Баг №10. Неверный код ответа при отправке запроса - Authors: удаление авторов id=0 некорректно

### Предусловие:

Открыть сайт https://fakerestapi.azurewebsites.net/index.html

Открыта секция Authors

### Шаги:

Отправить запрос: DELETE​/api​/v1​/Authors​/0

### ОЖ: 

- код 404 Not Found

Тело ответа пустое

Response Headers

access-control-allow-origin: *

api-supported-versions: 1.0

content-length: 0

date: Sat10 Jun 2023 13:19:11 GMT

server: Kestrel

### ФР: 

код 200

тело ответа: пустое

заголовки ответа:

 access-control-allow-origin: * 
  
  api-supported-versions: 1.0 
 
 content-length: 0 
 
 date: Tue13 Jun 2023 10:42:48 GMT 
 
 server: Kestrel

### Серьезность: Critical

### Окружение: MacBook Pro, MacOs 13.4, Google Chrome, Версия 114.0.5735.106



## CoverPhotos

## Баг №11. Неверный код ответа. CoverPhotos: создание "Фото на обложке" (тело запроса корректно)

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.

**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
с телом:
```
{
 "id": 201,
 "idBook": 201,
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Ожидаемый результат:** HTTP Status: `201 Created`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №12. Несохранение добавляемых данных. CoverPhotos: создание "Фото на обложке" (тело запроса корректно)

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
- Отправлен POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
с телом:
```
{
 "id": 201,
 "idBook": 201,
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201`

**Ожидаемый результат:** HTTP Status: `200 OK`  
**Фактический результат:** HTTP Status: `404 Not Found`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №13. Неверный код ответа. CoverPhotos: создание "Фото на обложке" (тело запроса некорректно)

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.

**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
с телом:
```
{
 "id": 1,
 "idBook": 1,
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

**Ожидаемый результат:** HTTP Status: `409 Conflict`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №14. Неверный код ответа. CoverPhotos: создание "Фото на обложке" (тело запроса некорректно - отправка пустых строк) код ответа 400

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.

**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
с телом:
```
{
   "idBook": 201,
   "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Ожидаемый результат:** HTTP Status: `400 Bad Request`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №15. Неверный код ответа. CoverPhotos: получение информации о книге с "Фото на обложке" (id некорректный) код ответа 404

**Серьезность:** S3 | Major  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/201`

**Ожидаемый результат:** HTTP Status: `404 Not Found`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №16. Несохранение редактируемых данных. CoverPhotos: изменение информации о "Фото на обложке" (тело запроса и id корректны) код ответа 200

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
- Отправлен POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`
с телом:
```
{
 "id": 1,
 "idBook": 1,
 "url": "а"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`
- Проверить код состояния: HTTP Status: `200 OK`

**Ожидаемый результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
 "id": 1,
 "idBook": 1,
 "url": "а"
}
```

**Фактический результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №17. Неверный код ответа. CoverPhotos: изменение информации о "Фото на обложке" (id в теле запроса заголовке не совпадают) код ответа 400

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
**Шаги:**
- Отправить PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/202`
с телом:
```
{
 "id": 201,
 "idBook": 201,
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Ожидаемый результат:** HTTP Status: `400 Bad Request`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №18. Неверный код ответа. CoverPhotos: создание "Фото на обложке" (тело запроса и id корректны) код ответа 201, метод PUT

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
**Шаги:**
- Отправить PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201`
с телом:
```
{
 "id": 201,
 "idBook": 201,
"url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Ожидаемый результат:** HTTP Status: `201 Created`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №19. Несохранение добавляемых данных. CoverPhotos: создание "Фото на обложке" (тело запроса и id корректны) код ответа 201, метод PUT

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
- Отправлен PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201`
с телом:
```
{
 "id": 201,
 "idBook": 201,
"url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201`

**Ожидаемый результат:** HTTP Status: `200 OK`  
**Фактический результат:** HTTP Status: `404 Not Found`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №20. Неудаление данных. CoverPhotos: удаление  "Фото на обложке" (id корректный) код ответа 200

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
- Отправлен DELETE запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`

**Ожидаемый результат:** HTTP Status: `404 Not Found`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №21. Неверный код ответа. CoverPhotos: удаление  "Фото на обложке" (id некорректный) код ответа 404

**Серьезность:** S3 | Major  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `CoverPhotos`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены CoverPhotos id со значениями 1-200.
**Шаги:**
- Отправить DELETE запрос:
`https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201`

**Ожидаемый результат:** HTTP Status: `404 Not Found`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

##Users

## Баг №22. Неверный код ответа. Users: создание пользователя (тело запроса корректно) код ответа 201

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users`
с телом:
```
{
 "id": 11,
 "userName": "User 11",
 "password": "Password11"
}
```

**Ожидаемый результат:** HTTP Status: `201 Created`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №23. Несохранение вводимых данных. Users: создание пользователя (тело запроса корректно) код ответа 201

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
- Отправлен POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users`
с телом:
```
{
 "id": 11,
 "userName": "User 11",
 "password": "Password11"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/11`

**Ожидаемый результат:** HTTP Status: `200 OK`  
**Фактический результат:** HTTP Status: `404 Not Found`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №24. Неверный код ответа. Users: создание пользователя (тело запроса некорректно) код ответа 409

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users`
с телом:
```
{
 "id": 1,
 "userName": "User 1",
 "password": "Password1"
}
```

**Ожидаемый результат:** HTTP Status: `409 Conflict`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №25. Неверный код ответа. Users: создание пользователя (тело запроса некорректно - отправка пустых строк) код ответа 400

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
**Шаги:**
- Отправить POST запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users`
с телом:
```
{
 "userName": "User 1",
 "password": "Password1"
}
```

**Ожидаемый результат:** HTTP Status: `400 Bad Request`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №26. Несохранение изменяемых данных. Users: изменение информации о пользователе (тело запроса и id корректны) код ответа 200

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
- Отправлен PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`
с телом:
```
{
 "id": 1,
 "userName": "User 1",
 "password": "а"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`

- Проверить код состояния: HTTP Status: `200 OK`
**Ожидаемый результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
 "id": 1,
 "userName": "User 1",
 "password": "а"
}
```

**Фактический результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```

**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №27. Несохранение изменяемых данных. Users: изменение информации о пользователе (тело запроса и id корректны, тело частичное) код ответа 200

**Серьезность:** S1 | Blocker  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
- Отправлен PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`
с телом:
```
{
 "id": 1,
 "userName": "User 1"
}
```

**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`

- Проверить код состояния: HTTP Status: `200 OK`
**Ожидаемый результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
 "id": 1,
 "userName": "User 1",
 "password": null
}
```

**Фактический результат:**
Тело ответа в формате JSON возвращается от сервера и имеет вид:
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```

**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №28. Неверный код ответа. Users: изменение информации о пользователе (id в теле запроса заголовке не совпадают) код ответа 400

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
**Шаги:**
- Отправить PUT запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/12`
с телом:
```
{
 "id": 11,
 "userName": "User 11",
 "password": "Password11"
}
```

**Ожидаемый результат:** HTTP Status: `400 Bad Request`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №29. Неудаление данных. Users: удаление пользователя (id корректный) код ответа 200

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.
- Отправлен DELETE запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`
**Шаги:**
- Отправить GET запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/1`

**Ожидаемый результат:** HTTP Status: `404 Not Found`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Баг №30. Неверный код ответа. Users: удаление пользователя (id некорректный) код ответа 404

**Серьезность:** S2 | Critical  
**Предшествующие условия:**
- Открыт сайт `https://fakerestapi.azurewebsites.net/index.html`
- Открыта секция `Users`
- Headers request:
  - Media-Type: application/json
  - accept: application/json
- На сервер добавлены Users id со значениями 1-10.

**Шаги:**
- Отправить DELETE запрос:
`https://fakerestapi.azurewebsites.net/api/v1/Users/11`

**Ожидаемый результат:** HTTP Status: `404 Not Found`  
**Фактический результат:** HTTP Status: `200 OK`  
**Окружение:** Windows 7 Ultimate; Firefox (версия 114.0.1)

## Books​

## Баг №31 Неправильный статус-код при удалении несуществующего ID в разделе Books в эндпоинте DELETE​/api​/v1​/Books​

### Предшествующие условия 

1. Открыт сайт Swagger UI https://fakerestapi.azurewebsites.net/index.html
2. открыт раздел Books 
3. Нажат эндпоинт DELETE​/api​/v1​/Books​

### Серьезность
Severity: Minor

### Шаги для воспроизведения
1. Отправить DELETE запрос
https://fakerestapi.azurewebsites.net/api/v1/Books/2000

### Ожидаемый результат 
В системе появились строки Cirl,Request URL Код 404, Error: Not Found. Книга не найдена.

### Фактический результат
В системе появились строки Cirl,Request URL Код 200. Книга успешно удалена.

### Окружение 
Google Chrome Версия 114.0.5735.110 (Официальная сборка), (64 бит)

## Баг №32. Неверный статус-код. Books: изменение информации о несуществующей книге id=201 в эндпоинте PUT​/api​/v1​/Books​/{id}

### Предшествующие условия  

1. Открыт сайт Swagger UI https://fakerestapi.azurewebsites.net/index.html
2. открыт раздел Books 
3. Нажат эндпоинт PUT​/api​/v1​/Books​/{id}​

### Серьезность
Severity: Minor

### Шаги для воспроизведения
1. Отправить PUT запрос:

https://fakerestapi.azurewebsites.net/api/v1/Books/201

С телом:
```
{
  "id": 201,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T17:09:12.622Z"
}
```
### Ожидаемый результат 

В системе появились строки Cirl,Request URL Код 404, Error: Not Found. Книга не найдена.

### Фактический результат

В системе появились строки Cirl,Request URL Код 200. Книга успешно изменена.

### Окружение 
Google Chrome Версия 114.0.5735.110 (Официальная сборка), (64 бит)
