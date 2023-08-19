# 1. GET /api​/v1​/Activities
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа (часть):
```
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-06T16:50:44.3254174+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-06-06T17:50:44.3254198+00:00",
    "completed": true
  },
```
# 2. POST /api​/v1​/Activities (id=0)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T16:04:07.198Z",
  "completed": true
}
```
Статус-код ответа: `200`
# 3. POST /api​/v1​/Activities (id=10000000000)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 10000000000,
  "title": "string",
  "dueDate": "2023-06-07T16:44:22.106Z",
  "completed": true
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-19b4fc0670519940904307668fb1258e-7b8bff6febceca46-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
# 4. GET /api​/v1​/Activities​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-06-06T17:07:04.2084647+00:00",
  "completed": false
}
```
# 5. GET /api​/v1​/Activities​/1000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/1000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `404`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-36489c49d3df05489261569291151da3-134c15484dac1342-00"
}
```
# 6. PUT ​/api​/v1​/Activities​/1
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T16:11:15.049Z",
  "completed": true
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T16:11:15.049Z",
  "completed": true
}
```
# 7. PUT ​/api​/v1​/Activities​/10000000000
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/10000000000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T16:11:15.049Z",
  "completed": true
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-228e892f2a6e9e418fa327e1f02334f1-3babf61803a4aa47-00",
  "errors": {
    "id": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 8. DELETE ​/api​/v1​/Activities​/1
HTTP-метод: `DELETE`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Activities/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`
# 9. GET ​/api​/v1​/Authors
HTTP-метод: `GET`   
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа (часть):
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
```
# 10. POST ​/api​/v1​/Authors (id=0)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: `200`
# 11. POST ​/api​/v1​/Authors (id=10000000000)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 10000000000,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-f29daf3409063e47b120a8c3433b30ac-618ea43d5ab2354f-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
# 12. GET ​/api​/v1​/Authors​/authors​/books​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  }
]
```
# 13. GET ​/api​/v1​/Authors​/authors​/books​/10000000000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/10000000000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c253d4739acf054c9df55ee1ffea4373-d96a58ee5b80024b-00",
  "errors": {
    "idBook": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 14. GET ​/api​/v1​/Authors​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}
```
# 15. GET ​/api​/v1​/Authors​/1000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/1000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `404`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-3b08df63fc14364bae1827443e62f9eb-1c5555cc21412941-00"
}
```
# 16. PUT ​/api​/v1​/Authors​/1
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
# 17. PUT ​/api​/v1​/Authors​/10000000000
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/10000000000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-233870bc23ef5e4a8f3973e190c7f5b1-79ea855e7a689a47-00",
  "errors": {
    "id": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 18. DELETE ​/api​/v1​/Authors​/1
HTTP-метод: `DELETE`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Authors/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`
# 19. GET ​/api​/v1​/Books
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа (часть):
```
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-05T16:36:35.4309683+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 200,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-04T16:36:35.430983+00:00"
  },
```
# 20. POST ​/api​/v1​/Books (id=0)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:37:57.305Z"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:37:57.305Z"
}
```
# 21. POST ​/api​/v1​/Books (id=10000000000)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ceeb6af9e5944c40a33bb2be868c3f6f-10bbf0798cb66341-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:37:57.305Z"
}
```
# 22. GET ​/api​/v1​/Books​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 1,
  "title": "Book 1",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 100,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-05T16:39:45.8622657+00:00"
}
```
# 23. GET ​/api​/v1​/Books​/1000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/1000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `404`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-e6e6d1858c0b5347a3c7adbd841ace1c-5ab67ede58d44541-00"
}
```
# 24. PUT ​/api​/v1​/Books​/1
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/1`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: text/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:42:11.949Z"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:42:11.949Z"
}
```
# 25. PUT ​/api​/v1​/Books​/10000000000
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/10000000000`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: text/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-06T16:42:11.949Z"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5e1c7bc2b480984799c3c13688d46d8f-8564ae58382d294f-00",
  "errors": {
    "id": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 26. DELETE ​/api​/v1​/Books​/1
HTTP-метод: `DELETE`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Books/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`
# 27. GET ​/api​/v1​/CoverPhotos
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа (часть):
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  },
```
# 28. POST ​/api​/v1​/CoverPhotos (id=0)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: text/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
# 29. POST ​/api​/v1​/CoverPhotos (id=10000000000)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: text/json; v=1.0"`  
Тело запроса:
```
{
  "id": 10000000000,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-44edd5e25e58d445b23e7ab936d9ba7e-92590a11b853cc4b-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
# 30. GET ​/api​/v1​/CoverPhotos​/books​/covers​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
]
```
# 31. GET ​/api​/v1​/CoverPhotos​/books​/covers​/10000000000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/10000000000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-3f20afea0b004243a20d09ad5c349bae-c86b197a1964ed4c-00",
  "errors": {
    "idBook": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 32. GET ​/api​/v1​/CoverPhotos​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
# 33. GET ​/api​/v1​/CoverPhotos​/1000
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `404`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-ca6f70be1450724da16c55b47edaa851-1fcbe8c16b6d9146-00"
}
```
# 34. PUT ​/api​/v1​/CoverPhotos​/1
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
# 35. PUT ​/api​/v1​/CoverPhotos​/10000000000
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10000000000`  
Заголовки запроса: `"accept: text/plain; v=1.0"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-27de1b0cad96c54ebaf32c0621f95dda-349c449d20bec142-00",
  "errors": {
    "id": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 36. DELETE ​/api​/v1​/CoverPhotos​/1
HTTP-метод: `DELETE`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`
# 37. GET ​/api​/v1​/Users
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users`  
Заголовки запроса: `"accept: text/plain; v=1.0"`  
Статус-код ответа: `200`  
Тело ответа (часть):
```
[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
  {
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
  },
  {
    "id": 3,
    "userName": "User 3",
    "password": "Password3"
  },
```
# 38. POST ​/api​/v1​/Users (id=0)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
# 39. POST ​/api​/v1​/Users (id=10000000000)
HTTP-метод: `POST`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 10000000000,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-9e3e48be4f8c694d960f1369176af6d8-bd9f5dfdf911f944-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
# 40. GET /api​/v1​/Users​/1
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```
# 41. GET /api​/v1​/Users​/100
HTTP-метод: `GET`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/100`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `404`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-ab44af8620b66a4183bfc38d6d692b73-7f222c5f6717404a-00"
}
```
# 42. PUT ​/api​/v1​/Users​/1
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/1`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: `200`  
Тело ответа:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
# 43. PUT ​/api​/v1​/Users​/10000000000
HTTP-метод: `PUT`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/10000000000`  
Заголовки запроса: `"accept: */*"`, `"Content-Type: application/json; v=1.0"`  
Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: `400`  
Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ac18efbaf514fd4896ff6368a7569789-a37b7a83bc20ed4a-00",
  "errors": {
    "id": [
      "The value '10000000000' is not valid."
    ]
  }
}
```
# 44. DELETE ​/api​/v1​/Users​/1
HTTP-метод: `DELETE`  
Полный URL запроса: `https://fakerestapi.azurewebsites.net/api/v1/Users/1`  
Заголовки запроса: `"accept: */*"`  
Статус-код ответа: `200`
