Поле Username:
- пустое Поле
- невалидное значение, например sdf123
- валидные значения  - standard_user, locked_out_user, problem_user, performance_glitch_user

Поле password
 - пустое поле
  - невалидное значение, например qwerty
  - валидное значение - secret_sauce

## Проверка авторизации на сайте методом попарного тестирования
|номер тест кейса| предшествующие условия | шаг1  вводим username | шаг2 вводим password | шаг 3 | ожидаемый результат |
| ------ | ------ | ----- | ----- | ------ | ------- |
|1| Перейди по ссылке https://www.saucedemo.com/ | пустое | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username is required |
|2| Перейди по ссылке https://www.saucedemo.com/ | sdf123 | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Password is required |
|3| Перейди по ссылке https://www.saucedemo.com/ | standard_user | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Password is required |
|4| Перейди по ссылке https://www.saucedemo.com/ | locked_out_user | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Password is required |
|5| Перейди по ссылке https://www.saucedemo.com/ | problem_user | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Password is required |
|6| Перейди по ссылке https://www.saucedemo.com/ | performance_glitch_user | пустое | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Password is required |
|7| Перейди по ссылке https://www.saucedemo.com/ | пустое | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username is required |
|8| Перейди по ссылке https://www.saucedemo.com/ | sdf123 | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|9| Перейди по ссылке https://www.saucedemo.com/ | standard_user | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|10| Перейди по ссылке https://www.saucedemo.com/ | locked_out_user | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|11| Перейди по ссылке https://www.saucedemo.com/ | problem_user | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|12| Перейди по ссылке https://www.saucedemo.com/ | performance_glitch_user | qwerty | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|13| Перейди по ссылке https://www.saucedemo.com/ | пустое | secret_sauce | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username is required |
|14| Перейди по ссылке https://www.saucedemo.com/ | sdf123 | secret_sauce | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Username and password do not match any user in this service |
|15| Перейди по ссылке https://www.saucedemo.com/ | standard_user | secret_sauce | Нажать на кнопку "LOGIN" | успешная авторизация |
|16| Перейди по ссылке https://www.saucedemo.com/ | locked_out_user | secret_sauce | Нажать на кнопку "LOGIN" | ошибка - Epic sadface: Sorry, this user has been locked out. |
|17| Перейди по ссылке https://www.saucedemo.com/ | problem_user | secret_sauce | Нажать на кнопку "LOGIN" | успешная авторизация |
|18| Перейди по ссылке https://www.saucedemo.com/ | performance_glitch_user | secret_sauce | Нажать на кнопку "LOGIN" | успешная авторизация |
