# Баг-репорты

## Баг №1. Неверное сообщение при вводе корректных данных
При вводе корректных данных на странице авторизации выводится неверное сообщение в неверном месте.
**Серьезность:** S4 | Blocker
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. В поле `Username` ввести логин `admin`
2. В поле `Password` ввести пароль `admin`
3. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выводится сообщение `Logged In Successfully` над кнопкой `Log in`
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull` в верху страницы
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №2. Неверное сообщение при верном логине и пустом пароле
При вводе верного логина и незаполнении поля пароля выводится неверное сообщение в неверном месте.
**Серьезность:** S0 | Trivial
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. В поле `Username` ввести логин `admin`
2. Поле `Password` оставить пустым
3. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выводится сообщение `Enter Both Username And Password` над кнопкой `Log in`
**Фактический результат:** Выводится сообщение `Please enter bouth username and password` в верху страницы
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №3. Неверное сообщение при пустом логине и верном пароле
При незаполнении поля логина и вводе верного пароля выводится неверное сообщение в неверном месте.
**Серьезность:** S0 | Trivial
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. Поле `Username` оставить пустым
2. В поле `Password` ввести пароль `admin`
3. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выводится сообщение `Enter Both Username And Password` над кнопкой `Log in`
**Фактический результат:** Выводится сообщение `Please enter bouth username and password` в верху страницы
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №4. Неверное сообщение при верном логине и неверном пароле
При вводе верного логина и неверного пароля выводится неверное сообщение в неверном месте.
**Серьезность:** S2 | Major
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. В поле `Username` ввести логин `admin`
2. В поле `Password` ввести пароль `qqq`
3. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выводится сообщение `Incorrect password` над кнопкой `Log in`
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull` в верху страницы
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №5. Неверное сообщение при неверном логине и верном пароле
При вводе неверного логина и верного пароля выводится неверное сообщение в неверном месте.
**Серьезность:** S2 | Major
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. В поле `Username` ввести логин `admin`
2. В поле `Password` ввести пароль `admin`
3. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выводится сообщение `Username Not Found` над кнопкой `Log in`
**Фактический результат:** Выводится сообщение `Username not foundLog in successfull` в верху страницы
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome

## Баг №6. Сброс языка при авторизации
При смене языка и попытке авторизации язык сбрасывается
**Серьезность:** S1 | Minor
**Предшествующие условия:** Открыта страница авторизации `testingchallenges.thetestingmap.org/login/login.php`
**Шаги:**
1. В поле `Username` ввести логин `admin`
2. В поле `Password` ввести пароль `admin`
3. Нажать на один из вариантов языка:
  - French
  - Italian
  - German
4. Нажать на кнопку `Log in`
**Ожидаемый результат:** Выбранный язык не сбрасывается после попытки авторизации
**Фактический результат:** После смены языка на французский, итальянский, немецкий и авторизации, форма возвращается к английскому языку
**Окружение:** Windows 7 Ultimate/Windows 10/Windows 10 Pro/Windows 11; Firefox/Google Chrome
