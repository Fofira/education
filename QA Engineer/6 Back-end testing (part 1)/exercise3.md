## Коды ответов
### **Код ответа: ~~201~~ 200.**
Тело ответа:
>[
    {
        "name": "Малышева Екатерина Матвеевна",
        "birthday": "1995-06-01",
        "post": "Бухгалтер"
    },
    {
        "name": "Капустин Роман Артёмович",
        "birthday": "1991-01-18",
        "post": "Финансовый аналитик"
    },
    {
        "name": "Касьянов Ярослав Ярославович",
        "birthday": "1989-07-29",
        "post": "Кредитный эксперт"
    },
    {
        "name": "Белова Елизавета Руслановна",
        "birthday": "1997-04-13",
        "post": "Аудитор"
    },
    {
        "name": "Романов Константин Александрович",
        "birthday": "2001-12-14",
        "post": "Кассир"
    },
    ...
]

- **200** - OK (Хорошо) - Возвращается в случае успешной обработки запроса, при этом тело ответа обычно содержит запрошенный ресурс.
- **201** - Created (Создано) - В результате успешного выполнения запроса был создан новый ресурс. Сервер может указать адреса (их может быть несколько) созданного ресурса в теле ответа, при этом предпочтительный адрес указывается в заголовке Location. Тело ответа чаще всего пустое, так как информация содержится в заголовке.

### **Код ответа: ~~400~~ 401.**
Тело ответа:

>{
  "message": "Неверные данные для авторизации."
}

-  **401** - Unauthorized — Сообщает о необходимости быть авторизованным для получения запрашиваемого доступа. Возникает при неправильном вводе данных пользователем при авторизации.
-  **400** - Bad Request (Неправильный запрос) - можно увидеть, если запрос был сформирован с ошибками.

### **Код ответа: ~~500~~ 400.**
Тело ответа:

>{
  "message": "Неверно составлен запрос."
}

-  **400** - Bad Request (Неправильный запрос) - можно увидеть, если запрос был сформирован с ошибками.
-  **500** - Internal Error (Внутренняя ошибка сервера) -	возвращается сервером, когда он не может по определенным причинам обработать запрос.