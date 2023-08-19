## Эндпоинты

1. **GET/api/v1/new-year/recipes/**  
  Получение списка всех новогодних рецептов.  
  URL: https://gotovim.net/api/v1/new-year/recipes
2. **POST/api/v1/new-year/recipes/**  
  Создание нового рецепта.  
  Тело:
  ```
  {
    "id": 5,
    "title": "string",
    "ingridients": "string",
    "description": "string",
    "publishDate": "2023-06-05T17:23:08.479Z"
  }
  ```  

3. **PATCH/api/v1/new-year/recipes/1**  
  Редактирование новогоднего рецепта "1"  
  URL: https://gotovim.net/api/v1/new-year/recipes/1  
  Тело:
  ```
  {
    "title": 'Новый заголовок'
  }
```

4. **DELETE/api/v1/new-year/recipes/1**  
  Удаление новогоднего рецепта "1".  
  URL: https://gotovim.net/api/v1/new-year/recipes/1
