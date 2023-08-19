 ## Activities

##  № 1. GET/api /v1 /Activities

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities

2. Ожидаемый результат: код 200, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: bf5b972c-de1f-44bf-8391-c0fe28e2108b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 14:33:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа (если  есть):

[
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-13T15:33:35.2059363+00:00",
        "completed": false
    }, …


##  № 2. POST/api /v1 /Activities 

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Activities

2. Ожидаемый результат: код 201, тест пройден.

3. Заголовки запроса: 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: f02087a5-1c73-4272-b12b-87f9882ea204
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 113

4. Тело запроса (если есть):

 {
  "id": 31,
  "title": "Activity 31",
  "dueDate": "2023-06-14T14:46:44.2536687+00:00",
  "completed": true
 }

5. Заголовки ответа: 

Content-Length: 0
Date: Tue, 13 Jun 2023 14:24:44 GMT
Server: Kestrel

6. Тело ответа (если  есть): 

{
    "id": 31,
    "title": "Activity 31",
    "dueDate": "2023-06-14T14:46:44.2536687+00:00",
    "completed": true
}


##  № 3. POST/api /v1 /Activities 

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Activities

2. Ожидаемый результат: код 409, тест пройден.

3. Заголовки запроса: 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 58c6881b-4afe-4394-bd33-571cfdcf6426
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 103

4. Тело запроса (если есть):

{
  "id": ,
  "title": "Activity 1",
  "dueDate": "2023-06-10T13:28:13.4432704+00:00",
  "completed":
}

5. Заголовки ответа: 

Content-Length: 0
Date: Tue, 13 Jun 2023 14:24:56 GMT
Server: Kestrel

6. Тело ответа (если  есть): 

{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ceef8e05c9f27f4db0393a87a6b55ca5-54251fac36e07e46-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
        ]
    }
}


##  № 4. GET/api /v1 /Activities /1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

2. Ожидаемый результат: код 200, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 8daef124-f8d7-48b3-a833-5162d703f690
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 14:49:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа (если  есть): 

{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-13T15:49:33.2103404+00:00",
    "completed": false
}


##  № 5. GET/api /v1 /Activities /-1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id_1}}

2. Ожидаемый результат: код 404, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 9a878a10-d139-4246-bf97-26edcd9f3ed1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 14:52:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа (если  есть): 

{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-6db2fcc81d61eb41893a1c439d54a936-291a188d5aec0646-00"
}


##  № 6. GET/api /v1 /Activities / 

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id_3}}

2. Ожидаемый результат: код 400, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: be4d6463-9c29-451c-a86f-6d4fa62c8881
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Type: application/problem+json; charset=utf-8
Date: Tue, 13 Jun 2023 14:54:51 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа (если  есть): 

{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-327c9c54f1ca3844aa566f4db5f96102-4304afb19c6ddc48-00",
    "errors": {
        "id": [
            "The value ' ' is invalid."
        ]
    }
}


##  № 7. PUT/api /v1 /Activities /1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

2. Ожидаемый результат: код 200, тест пройден.

3. Заголовки запроса: 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: afd38663-8404-43b0-afac-0baee40e5864
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 105

4. Тело запроса (если есть):

{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-06-10T13:28:13.4432704+00:00",
  "completed": false
}

5. Заголовки ответа: 

Content-Type: application/problem+json; charset=utf-8
Date: Tue, 13 Jun 2023 15:00:08 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа (если  есть): 

{"id":1,"title":"Activity 1","dueDate":"2023-06-10T13:28:13.4432704+00:00","completed":false}


##  № 8. PUT/api /v1 /Activities /0

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id_2}}

2. Ожидаемый результат: код 400, тест пройден.

3. Заголовки запроса: 

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 2222f214-1e96-4495-87b2-5cad985ab4c6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 110

4. Тело запроса (если есть):

{
  "id": 0,
  "title": "Activity 2",
  "dueDate": "2023-06-10T13:28:13.4432704+00:00",
  "completed": 
}

5. Заголовки ответа: 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 14:58:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа (если  есть): 

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-c78b053e344ed84fbcba9cf999668bcd-c256eacc42307040-00","errors":{"$.completed":["'}' is an invalid start of a value. Path: $.completed | LineNumber: 5 | BytePositionInLine: 0."]}}


##  № 9. PUT/api /v1 /Activities /0

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

2. Ожидаемый результат: код 415, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 8df876e8-8c30-4741-825e-74c93c9fbfa4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0

4. Тело запроса (если есть): пустое

5. Заголовки ответа: 

Content-Type: application/problem+json; charset=utf-8
Date: Tue, 13 Jun 2023 15:03:35 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа (если  есть): 

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13","title":"Unsupported Media Type","status":415,"traceId":"00-1ab7a1245baa8542aa1c80c3ec6fbd21-f96e789c0bd4ff4b-00"}


##  № 10. DELETE/api /v1 /Activities /1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

2. Ожидаемый результат: код 200, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 2dd74333-1de1-46e7-84e3-89c7895eb80c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Length: 0
Date: Tue, 13 Jun 2023 15:06:04 GMT
Server: Kestrel
api-supported-versions: 1.0

6. Тело ответа (если  есть):  нет


##  № 11. DELETE/api /v1 /Activities /0

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id_2}}

2. Ожидаемый результат: код 404, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 477e147a-bf63-4100-8f9b-ccd3a46ec46b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Length: 0
Date: Tue, 13 Jun 2023 15:07:49 GMT
Server: Kestrel
api-supported-versions: 1.0

6. Тело ответа (если  есть):  нет


## Authors

##  № 12. GET/api /v1 /Authors

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id_2}}

2. Ожидаемый результат: код 200, тест пройден.

3. Заголовки запроса: 

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 26cfc8e6-cd35-4e3b-a3c4-7c1e87151f85
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса (если есть): нет

5. Заголовки ответа: 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 15:11:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа (если  есть): 

[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },



##  № 13. POST/api/v1/Authors 

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors

2. Ожидаемый результат: код 201, тест пройден.

3. Заголовки запроса:

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 37010a3b-8187-43f0-92da-c966bc7089df
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 94

4. Тело запроса:

{
  "id": 600,
  "idBook": 1,
  "firstName": "First Name 600",
  "lastName": "Last Name 600"
}

5. Заголовки ответа:

Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 13 Jun 2023 15:31:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа:

{"id":600,"idBook":1,"firstName":"First Name 600","lastName":"Last Name 600"}


##  № 14. POST/api/v1/Authors 

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors

2. Ожидаемый результат: код 409, тест пройден.

3. Заголовки запроса:

Request Headers
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: f433e5a0-e11e-47a2-b34e-d3a7eeb75f08
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 78

4. Тело запроса:

{
  "id": 600,
  "idBook": 1,
  "firstName": "First Name 600",
  "lastName":
}

5. Заголовки ответа:

Content-Type: application/problem+json; charset=utf-8
Date: Tue, 13 Jun 2023 16:17:51 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа:

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-bba7dc4782e1ff4fb6f213bfd31ce560-ae153b5840b7754f-00","errors":{"$.lastName":["'}' is an invalid start of a value. Path: $.lastName | LineNumber: 5 | BytePositionInLine: 0."]}}


##  № 15. POST/api/v1/Authors 

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors

2. Ожидаемый результат: 415, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: ac426392-c2cf-4b68-96a3-60b5f2edc4af
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0

4. Тело запроса: нет

5. Заголовки ответа:

Content-Type: application/problem+json; charset=utf-8
Date: Tue, 13 Jun 2023 16:20:27 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа:

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13","title":"Unsupported Media Type","status":415,"traceId":"00-3e9e65b58c812d4199d7cd4c9c7e09e0-efdf3f9b1ff0e442-00"}


##  № 16. PUT/api /v1 /Authors /1

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Authors​/{{activity_id}}

2. Ожидаемый результат: 200, тест пройден

3. Заголовки запроса:

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: d7e91df1-b29b-42e7-ba13-e55a1dd30ef5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 90

4. Тело запроса: 

{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 344"
}

5. Заголовки ответа:

Content-Length: 0
Date: Tue, 13 Jun 2023 16:28:09 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 17. PUT/api /v1 /Authors /0

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Authors​/{{activity_id_2}}

2. Ожидаемый результат: 400, тест пройден

3. Заголовки запроса:

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 82eba8e1-62c6-4ef5-912f-cd0bfc2be3b8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 74

4. Тело запроса: 

{
  "id": 0,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName":
}

5. Заголовки ответа:

Content-Length: 0
Date: Tue, 13 Jun 2023 16:29:45 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 18. PUT/api /v1 /Authors /1

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Authors​/{{activity_id}}

2. Ожидаемый результат: 404, тест пройден

3. Заголовки запроса:

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 420934a3-b591-4c01-93fe-4f18aeb8939b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 74

4. Тело запроса: 

{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName":
}

5. Заголовки ответа:

Content-Length: 0
Date: Tue, 13 Jun 2023 16:31:37 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 19. PUT/api /v1 /Authors /0

1. URL: https://fakerestapi.azurewebsites.net/api​/v1​/Authors​/{{activity_id_2}}

2. Ожидаемый результат: 404, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: bd717783-c65e-4ca0-b4a9-1e66e63fb620
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Length: 0
Date: Wed, 14 Jun 2023 17:37:24 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 20. PUT/api /v1 /Authors /1

1. URL: https://fakerestapi.azurewebsites.net/index.html/api​/v1​/Authors​/{{activity_id}}

2. Ожидаемый результат: 404, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 6651610b-a091-4b80-903d-ee58f38ed12d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Length: 0
Date: Wed, 14 Jun 2023 17:41:04 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 21. GET/api /v1 /Authors /1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/{{activity_id}}

2. Ожидаемый результат: 200, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 24b438d6-22d9-4fa4-a65d-8c01c6ae3862
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 17:43:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа:

{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
}


##  № 22. GET/api /v1 /Authors /0

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors​/{{activity_id_2}}

2. Ожидаемый результат: 404, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 756991e6-f0d6-495d-9f99-26bca104e600
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Length: 0
Date: Wed, 14 Jun 2023 17:46:06 GMT
Server: Kestrel

6. Тело ответа: Нет


##  № 23. GET/api/v1/Authors/authors/books/1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{activity_id}}

2. Ожидаемый результат: 200, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: ed5fc412-8e8c-44ab-8e3d-688ea4489638
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 17:48:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа:

[{"id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"},{"id":2,"idBook":1,"firstName":"First Name 2","lastName":"Last Name 2"},{"id":3,"idBook":1,"firstName":"First Name 3","lastName":"Last Name 3»}]


##  № 24. GET/api/v1/Authors/authors/books/-1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{activity_id_1}}

2. Ожидаемый результат: 400, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 88192e55-66bf-4420-a8ba-3e1dd8ae96c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 17:50:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа:

[]

##  № 25. GET/api/v1/Authors/authors/books/ 

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{activity_id_3}}

2. Ожидаемый результат: 400, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: 6ca03bb7-fb29-475f-aa62-50bc0048e845
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Type: application/problem+json; charset=utf-8
Date: Wed, 14 Jun 2023 17:52:10 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа:

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-4e4968e6784aa349a57dd8c1081170e8-e14ced84865a9345-00","errors":{"idBook":["The value ' ' is invalid.»]}}


##  № 26. DELETE/api /v1 /Authors /1

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/{{activity_id}}

2. Ожидаемый результат: 200, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: c5c50c08-e2ee-4446-aec2-40cea89162a2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Length: 0
Date: Wed, 14 Jun 2023 18:03:15 GMT
Server: Kestrel
api-supported-versions: 1.0

6. Тело ответа: Нет


##  № 27. DELETE/api /v1 /Authors /0

1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors​/{{activity_id_2}}

2. Ожидаемый результат: 404, тест пройден

3. Заголовки запроса:

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Postman-Token: d1470f49-6551-4864-997c-d12c4d05a4d3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса: Нет

5. Заголовки ответа:

Content-Length: 0
Date: Wed, 14 Jun 2023 18:05:44 GMT
Server: Kestrel

6. Тело ответа:Нет


## Books

№28. Получение списка книг

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books 

2. ожидаемый результат

код 200, тест пройден  

3. Заголовки запроса

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3c081f29-9250-479e-9396-7db032fbd35c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

 отсутствует

5. Заголовок ответа

Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 16 Jun 2023 19:23:03 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
6. Тело ответа 

[
 {
  "id": 1,
  "title": "Book 1",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 100,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-11T08:33:58.1624062+00:00"
 },
........
{
 "id": 200,
 "title": "Book 200",
 "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
 "pageCount": 20000,
 "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
 "publishDate": "2022-11-24T08:33:58.1719072+00:00"
}
]


### №29. Создание списка книг (код 201)

URL

https://fakerestapi.azurewebsites.net/api/v1/Books 

2. ожидаемый результат

код 201, тест пройден

3. Заголовки запроса

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 715b2bad-d39f-426e-b838-de9975d07012
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

{
  "id": 201,
  "title": "Book 201",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 800,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-05T08:33:07.1901417+00:00"
 }

5. Заголовок ответа

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:02:49 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа 

{
  "id": 201,
  "title": "Book 201",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 800,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-05T08:33:07.1901417+00:00"
 }


## №30. Создание списка книг (код 400)

URL - https://fakerestapi.azurewebsites.net/api/v1/Books 

2. ожидаемый результат

код 400, тест пройден
3. Заголовки запроса

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cd6a3bad-ecbe-4f36-92c4-d6fa3ab90ca9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

{
 "id": +,
 "title": "string",
 "description": "string",
 "pageCount": 0,
 "excerpt": "string",
 "publishDate": "2023-06-12T08:56:17.303Z"
}

5. Заголовок ответа

Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:02:04 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9115bb9ca661ed4e8c5d8821622faec1-ccaa054b4fbb264c-00",
    "errors": {
        "$.id": [
            "'+' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}


## №31. получение информации о книге id=1 (код 200)

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/1 

2. ожидаемый результат

код 200, тест пройден

3. Заголовки запроса

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c1b74085-e172-4461-9b40-78f6e89958c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

отсутствует

5. Заголовок ответа
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:27:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа

{
  "id": 1,
  "title": "Book 1",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 100,
 "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-11T09:07:29.7367956+00:00"
}


## №32. Получение информации о книге id=1 (код 200)

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/-1 

2. ожидаемый результат

код 404, тест пройден

3. Заголовки запроса

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 74752b19-8e87-4d35-9bab-be02e3f5bf82
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

отсутствует

5. Заголовок ответа

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:39:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-663b4cfe4ce9314b9f624cb6a63e759f-aeb5b818461ef144-00"
}
изменение активностей


## №33. Изменение информации о книге id 1 (код 200)

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/1 

2. ожидаемый результат

код 200, тест пройден

3. Заголовки запроса

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 139a6f43-88b3-4f1d-8c28-19adc4ea6f6d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса
{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T10:42:53.137Z"
}

5. Заголовок ответа

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:43:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

6. Тело ответа

{
    "id": 1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-17T10:42:53.137Z"
}


## №34. Изменение информации о книге id 201 (код 400)

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/201 

2. ожидаемый результат

код 400, тест пройден

3. Заголовки запроса

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2156f7a3-97dc-4a6a-a0d0-a6488717c832
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса
{
"id": 201,
"title": "Book 201",
"description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
"pageCount": 20000,
"excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
"publishDate": "2022-11-24T11:24:23.2886422+00:00"
}

5. Заголовок ответа

Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:50:42 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа

{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f5724269d002f94ab32ac99e24f8ff54-fa103a8c5dfcab46-00",
    "errors": {
        "$": [
            "'}' is invalid after a single JSON value. Expected end of data. Path: $ | LineNumber: 8 | BytePositionInLine: 0."
        ]
    }


## №35. Удаление книг id=1

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/1 

2. ожидаемый результат

код 200, тест пройден

3. Заголовки запроса

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f244a9b9-c307-489c-adea-907f36f61d12
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

отсутствует

5. Заголовок ответа

Content-Length: 0
Date: Sat, 17 Jun 2023 10:55:10 GMT
Server: Kestrel
api-supported-versions: 1.0

6. Тело ответа

отсутствует

## №36. Удаление книг id=2000

1. URL

https://fakerestapi.azurewebsites.net/api/v1/Books/2000 

2. ожидаемый результат

код 400, тест пройден

3. Заголовки запроса

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 5dca4941-6d98-4143-b659-836e8f52f748
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

4. Тело запроса

отсутствует

5. Заголовок ответа

Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:58:21 GMT
Server: Kestrel
Transfer-Encoding: chunked

6. Тело ответа

отсутствует.


## CoverPhotos

# 37. GET/api/v1/CoverPhotos

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 45721f08-896f-424d-8134-9e48867b604a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 08:47:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа (часть):
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
```

# 38. POST/api/v1/CoverPhotos

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0b9a4260-8089-4369-8244-ae442b6d30d8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_201}},
 "idBook": {{book_id_201}},
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 08:51:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 201,
    "idBook": 201,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

# 39. POST/api​/v1​/CoverPhotos (incorrect body)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 17c81c7d-741e-4ab2-ab4e-06df4d71073f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 08:57:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

# 40. POST/api​/v1​/CoverPhotos (incorrect body-incorect JSON)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ad1e30ac-352c-4070-b8b8-65e6cea46447
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 08:58:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-37bc006f5151324485f4f5a1644bf7ca-c05c7b0c6c38184c-00",
    "errors": {
        "$.url": [
            "'h' is an invalid start of a value. Path: $.url | LineNumber: 3 | BytePositionInLine: 8."
        ]
    }
}
```

# 41. POST/api/v1/CoverPhotos (incorrect body-empty string)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 28a8d5e1-8e29-4672-9a4a-0baeca57b858
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
   "idBook": {{book_id_201}},
   "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:02:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 0,
    "idBook": 201,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

# 42. POST/api/v1/CoverPhotos (incorrect body-incorrect value type)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 075200a3-712f-4f99-847c-c4732732a651
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": "text",
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 09:09:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8018987fdee5da49b7972dc7291391fa-ef1946df66c5ba42-00",
    "errors": {
        "$.idBook": [
            "The JSON value could not be converted to System.Int32. Path: $.idBook | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```

# 43. POST/api/v1/CoverPhotos (incorrect body-empty)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `415 Unsupported Media Type`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4ebe88d4-12d0-4f5d-9ca3-31be24594eec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 09:12:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-1afec30b4e963c4e8812de7d029698f0-a9e55b632302b348-00"
}
```

# 44. POST/api/v1/CoverPhotos (incorrect body-id not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 89ecaa31-6ebd-4c71-8d6f-7bc3116bed4f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_10000000000}},
 "idBook": {{book_id_1}},
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 09:14:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-95c2ad55042b2c4585b2b342b084d0f7-1c4d576663701149-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

# 45. GET/api/v1/CoverPhotos/books/covers/{idBook}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ad844d2f-0a31-4505-a498-7c8ce96b6e5c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:17:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    }
]
```

# 46. GET/api/v1/CoverPhotos/books/covers/{idBook} (incorrect id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{book_id_201}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 454ae007-535e-43b1-8c65-eb59767a2fc2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:26:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
[]
```

# 47. GET/api/v1/CoverPhotos/books/covers/{idBook} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{book_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3321e3d9-fb55-4b81-8be3-394956613856
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 09:31:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c45c9d47d666f64cbf3faf1e5c4014de-b7bfdece3a244f48-00",
    "errors": {
        "idBook": [
            "The value '10000000000' is not valid."
        ]
    }
}
```

# 48. GET/api/v1/CoverPhotos/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 67ab7aed-34e7-43e2-a286-a79741c4f867
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:33:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

# 49. GET/api/v1/CoverPhotos/{id} (incorrect id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_201}}`
- Ожидаемый результат: `404 Not Found`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1142196b-6628-4577-8a12-f0ec20d37d51
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:38:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-7ca149508694bd46ac6e6a1a51be3cd2-21afd370cb7d5d4a-00"
}
```

# 50. GET/api/v1/CoverPhotos/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b26a1b45-18d5-441f-9a5d-fe6f2cc1dd92
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_10000000000}},
 "idBook": {{book_id_1}},
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 09:39:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b24cd9e6dbcb05478b7118927bf64a43-1540b6fcddf20f49-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```

# 51. PUT/api/v1/CoverPhotos/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 75d19228-1757-4630-966f-10286068e2f8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": "а"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:44:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": "а"
}
```

# 52. PUT/api/v1/CoverPhotos/{id} (empty string)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 692db20c-df7d-4731-9731-78d1c502a565
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}}
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 09:48:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "idBook": 1,
    "url": null
}
```

# 53. PUT/api/v1/CoverPhotos/{id} (different id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_202}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: dc504d04-bf5a-4f91-9475-89ad8bad8802
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_201}},
 "idBook": {{book_id_201}},
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:05:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 201,
    "idBook": 201,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

# 54. PUT/api/v1/CoverPhotos/{id} (incorrect body-incorrect JSON)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 51ed28f3-7811-40f6-b449-4382592a3cca
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": а
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:09:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ac7fcaf5548b354786a29b4b1a465788-3be718300efd334f-00",
    "errors": {
        "$.url": [
            "'0xD0' is an invalid start of a value. Path: $.url | LineNumber: 3 | BytePositionInLine: 8."
        ]
    }
}
```

# 55. PUT/api/v1/CoverPhotos/{id} (incorrect body-incorrect value type)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6b1f3ee4-8d0b-46b8-b85f-13069d49bfd9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": 1
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:11:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-844f1ab89e483b4b9583b5441df353b3-eb1e968fc1346a4f-00",
    "errors": {
        "$.url": [
            "The JSON value could not be converted to System.Uri. Path: $.url | LineNumber: 3 | BytePositionInLine: 9."
        ]
    }
}
```

# 56. PUT/api/v1/CoverPhotos/{id} (incorrect body-empty)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `415 Unsupported Media Type`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0a809573-788e-4fce-bc99-b8eb508574ac
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:12:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-63b8d5056334ea4b8afc8c6389e1bcef-2693c123043ae547-00"
}
```

# 57. PUT/api/v1/CoverPhotos/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b0551a82-2926-4ad6-96fc-103f73df6d22
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_1}},
 "idBook": {{book_id_1}},
 "url": "а"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:14:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4b32f89c7b0c844ea990f818dc13aaa5-7f3c6b74eeb63741-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```

# 58. PUT/api/v1/CoverPhotos/{id} (incorrect body-id not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2d136115-0973-47e4-813d-124d97ec3e99
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_10000000000}},
 "idBook": {{book_id_1}},
 "url": "а"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:16:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-038a9ffa84e8664689811e2fa48dfda1-8a5afdee1bd0a243-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

# 59. PUT/api/v1/CoverPhotos/{id} (create)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_201}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b6462027-3e92-41ac-86f0-5aca6efe81ba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_201}},
 "idBook": {{book_id_201}},
"url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:18:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 201,
    "idBook": 201,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

# 60. DELETE/api/v1/CoverPhotos/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9d8d438c-f666-4c63-b165-fcb266ec2696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 17 Jun 2023 10:19:48 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# 61. DELETE/api/v1/CoverPhotos/{id} (incorrect id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_201}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ca529ee5-4f95-4505-99e2-85709cdd33eb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 17 Jun 2023 10:21:15 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# 62. DELETE/api/v1/CoverPhotos/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 264a1a71-80da-4cb4-aaaa-ee0ce76bb15e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{coverphoto_id_201}},
 "idBook": {{book_id_201}},
"url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 201&w=250&h=350"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:22:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a199bd9486ab70478ab1d91842ab67d2-0497930b954f144c-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```


## Users

# 63. GET/api/v1/Users

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 5292e9e7-23f3-4e22-a303-e7c03ca26dbb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:23:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа (часть):
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
```

# 64. POST/api/v1/Users

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ae9bf76b-afd4-45d6-9389-208f756b6144
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_11}},
 "userName": "User 11",
 "password": "Password11"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:26:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 11,
    "userName": "User 11",
    "password": "Password11"
}
```

# 65. POST/api/v1/Users (incorrect body)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1434ed1c-0121-4690-894e-a400d58b1e09
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:28:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
}
```

# 66. POST/api/v1/Users (incorrect body-incorrect JSON)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6dd1f9d2-cb50-4ff8-a10d-b6a1227f6b01
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": Password1
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:30:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0771d30503323d448c419b7235495d7e-7b1900e7bb7b4645-00",
    "errors": {
        "$.password": [
            "'P' is an invalid start of a value. Path: $.password | LineNumber: 3 | BytePositionInLine: 13."
        ]
    }
}
```

# 67. POST/api/v1/Users (incorrect body-empty string)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0647f004-6415-4d90-8c60-6d97d7ece4f7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "userName": "User 1",
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 10:32:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 0,
    "userName": "User 1",
    "password": "Password1"
}
```

# 68. POST/api/v1/Users (incorrect body-incorrect value type)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d22753f6-e40a-4136-aa16-5f612ec3334f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": 1,
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:33:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1c9ec3767bcd4e48a909d80cea605d1f-646811a866ce1a43-00",
    "errors": {
        "$.userName": [
            "The JSON value could not be converted to System.String. Path: $.userName | LineNumber: 2 | BytePositionInLine: 14."
        ]
    }
}
```

# 69. POST/api/v1/Users (incorrect body-empty)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `415 Unsupported Media Type`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c8f6fb03-d4bf-46db-be3a-9fcb695c0d21
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 10:38:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-e746016e3109a843a978c7b381bf0c4d-dd85ea2683f31047-00"
}
```

# 70. POST/api/v1/Users (incorrect body-id not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cd78d5b2-41b3-4da2-83af-eeae1b06613e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_10000000000}},
 "userName": "User 1",
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:01:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-56750cd896ff3e4491302e89f74606dd-a48b40d114f97c40-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

# 71. GET/api/v1/Users/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e6c9420f-9afb-41d3-b9ff-76f9ebeafd88
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:03:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
}
```

# 72. GET/api/v1/Users/{id} (incorrect id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_11}}`
- Ожидаемый результат: `404 Not Found`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ac95b9bc-8d62-4336-8040-304b7b0fda3c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:11:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-2ca6fdf94bfe864a852e4aeaf093de1d-42629bc60d9dc84d-00"
}
```

# 73. GET/api/v1/Users/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 60595975-c1c5-49a0-8cf7-e2d450c1bbb9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:14:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6b919134cf29ba448badb3d8ad0015fa-a74aa93c762b0f4e-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```

# 74. PUT/api/v1/Users/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f47f3f65-3840-45e8-aa67-72f16a468556
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": "а"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:15:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": "а"
}
```

# 75. PUT/api​/v1​/Users​/{id} (empty string)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9a283fbd-0ccb-471c-8073-d3ab0036f2e6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:20:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 1,
    "userName": "User 1",
    "password": null
}
```

# 76. PUT/api​/v1​/Users​/{id} (different id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_12}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: aec1f3a0-4de7-401d-8d64-8ee5028cfedb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_11}},
 "userName": "User 11",
 "password": "Password11"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:21:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 11,
    "userName": "User 11",
    "password": "Password11"
}
```

# 77. PUT/api/v1/Users/{id} (incorrect body-incorrect JSON)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c12a9e3e-15e8-4d12-b68c-bf66057e8618
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": Password1
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:24:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c156483256e166408fee436756bb0eed-5f11514010c2b846-00",
    "errors": {
        "$.password": [
            "'P' is an invalid start of a value. Path: $.password | LineNumber: 3 | BytePositionInLine: 13."
        ]
    }
}
```

# 78. PUT/api/v1/Users/{id} (incorrect body-incorrect value type)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 63d9e527-bd1d-49fa-8520-7d876c052472
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": 1
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:26:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-eb49917c3592c34898b2c629141b5604-fb769ddf1d435b43-00",
    "errors": {
        "$.password": [
            "The JSON value could not be converted to System.String. Path: $.password | LineNumber: 3 | BytePositionInLine: 14."
        ]
    }
}
```

# 79. PUT/api/v1/Users/{id} (incorrect body-empty)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `415 Unsupported Media Type`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 73d1a851-8b65-4276-99b3-3791eb5e9ed7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:27:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-550edec15731b44c9bedf23b9c546562-369b5e0d5c705442-00"
}
```

# 80. PUT/api/v1/Users/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0ef58aa6-0bf4-495f-b0b1-53e38e4c7346
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_1}},
 "userName": "User 1",
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:29:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d01e53ae7705cb4c87e5fbd53cc2a668-b225e56cd85e034c-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```

# 81. PUT/api/v1/Users/{id} (incorrect body-id not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a863d78e-060f-4073-9c1a-9bb69b68f196
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
 "id": {{user_id_10000000000}},
 "userName": "User 1",
 "password": "Password1"
}
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:31:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2d7bf3bb5b211f45a89819706a8c2266-51c0bc7a803e104d-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```

# 82. PUT/api/v1/Users/{id} (create)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_11}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 74b78dfa-e4c0-48f4-9ab4-dee8fe71dd4f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Тело запроса:
```
{
"id": {{user_id_11}},
"userName": "User 11",
"password": "Password11"
}
```

- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 13:33:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```

- Тело ответа:
```
{
    "id": 11,
    "userName": "User 11",
    "password": "Password11"
}
```

# 83. DELETE/api/v1/Users/{id}

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_1}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cd3550fe-3628-41ec-8003-e1be9c199d58
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 17 Jun 2023 13:36:41 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# 84. DELETE/api/v1/Users/{id} (incorrect id)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_11}}`
- Ожидаемый результат: `200 OK`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 01fcf469-4538-4982-8b93-899b692c27a4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 17 Jun 2023 13:36:41 GMT
Server: Kestrel
api-supported-versions: 1.0
```

# 85. DELETE/api/v1/Users/{id} (incorrect id-not valid)

- URL: `https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_id_10000000000}}`
- Ожидаемый результат: `400 Bad Request`
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 46a1fdc6-b12e-45eb-817b-072de2e3e069
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 17 Jun 2023 13:55:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```

- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0df74d9054eeec4980cabf456d93fb9b-0db11360318ac444-00",
    "errors": {
        "id": [
            "The value '10000000000' is not valid."
        ]
    }
}
```



