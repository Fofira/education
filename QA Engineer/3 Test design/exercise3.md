# Возможные значения полей:
1. Username:
  - Пустое
  - Неверное
  - Верное:
    - standard_user
    - locked_out_user
    - problem_user
    - performance_glitch_user
2. Password:
  - Пустое
  - Неверное
  - Верное: secret_sauce

# Тест-кейсы
## Тест-кейс №1 — Прохождение авторизации с пустым значением Username и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - поле "Username" оставить пустым
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username is required"

## Тест-кейс №2 — Прохождение авторизации с пустым значением Username и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - поле "Username" оставить пустым
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username is required"

## Тест-кейс №3 — Прохождение авторизации с пустым значением Username и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - поле "Username" оставить пустым
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username is required"

## Тест-кейс №4 — Прохождение авторизации с неверным значением Username и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести неверный логин: `fff`
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Password is required"

## Тест-кейс №5 — Прохождение авторизации с неверным значением Username и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести неверный логин: `fff`
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №6 — Прохождение авторизации с неверным значением Username и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести неверный логин: `fff`
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №7 — Прохождение авторизации с верным значением Username (standard_user) и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `standard_user`
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Password is required"

## Тест-кейс №8 — Прохождение авторизации с верным значением Username (standard_user) и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `standard_user`
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №9 — Прохождение авторизации с верным значением Username (standard_user) и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `standard_user`
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - происходит авторизация (переход на страницу со списком товаров www.saucedemo.com/inventory.html)

## Тест-кейс №10 — Прохождение авторизации с верным значением Username (locked_out_user) и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `locked_out_user`
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Password is required"

## Тест-кейс №11 — Прохождение авторизации с верным значением Username (locked_out_user) и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `locked_out_user`
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №12 — Прохождение авторизации с верным значением Username (locked_out_user) и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `locked_out_user`
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Sorry, this user has been locked out."

## Тест-кейс №13 — Прохождение авторизации с верным значением Username (problem_user) и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `problem_user`
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Password is required"

## Тест-кейс №14 — Прохождение авторизации с верным значением Username (problem_user) и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `problem_user`
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №15 — Прохождение авторизации с верным значением Username (problem_user) и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `problem_user`
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - происходит авторизация (переход на страницу со списком товаров www.saucedemo.com/inventory.html)

## Тест-кейс №16 — Прохождение авторизации с верным значением Username (performance_glitch_user) и пустым значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `performance_glitch_user`
  - поле "Password" оставить пустым
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Password is required"

## Тест-кейс №17 — Прохождение авторизации с верным значением Username (performance_glitch_user) и неверным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `performance_glitch_user`
  - в поле "Password" ввести неверный пароль: `fff`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - авторизация не происходит
  - под полем ввода пароля появляется ошибка "Epic sadface: Username and password do not match any user in this service"

## Тест-кейс №18 — Прохождение авторизации с верным значением Username (performance_glitch_user) и верным значением Password
1. Предшествующие условия:
  - открыта страница авторизации (сайт www.saucedemo.com)
2. Шаги:
  - в поле "Username" ввести верный логин: `performance_glitch_user`
  - в поле "Password" ввести верный пароль: `secret_sauce`
  - нажать на кнопку "LOGIN"
3. Ожидаемый результат:
  - происходит авторизация (переход на страницу со списком товаров www.saucedemo.com/inventory.html)
