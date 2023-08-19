**Поля для ввода текста**
## Выбор полиса

 - кнопка «квартира»
 //button/span[text()=' Квартира ']
 - кнопка «дом»
//button/span[text()=' Дом ']

- Сдается в аренду:
  - кнопка «да»
 //div[text() = 'Сдается в аренду']/following::button[1] 
  - кнопка «нет»
 //div[text() = 'Сдается в аренду']/following::button[2] 

- Расположена на первом или последнем этаже:
  - кнопка «да» 
//div[text() = 'Расположена на первом или последнем этаже']/following::button[1] 
  - кнопка «нет»
 //div[text() = 'Расположена на первом или последнем этаже']/following::button[2]  
 
- Установлена Охранная сигнализация:
  - кнопка «да»
 //div[text() = 'Установлена охранная сигнализация']/following::button[1]
  - кнопка «нет»
 //div[text() = 'Установлена охранная сигнализация']/following::button[2]

- Материал несущих стен, появляются, если выбрать дом:
  - кнопка «кирпич или монолит»
//button/span[text()=' Кирпич или монолит ']
  - кнопка «дерево»
//button/span[text()=' Дерево ']

 - кнопка «применить»
//button/span[text()=' Применить ']

 - кнопка «оформить»
//button/span[text()=' Оформить ']
- Регион проживания
//input[@formcontrolname = 'registrationRegion']
- Промокод
//input[@formcontrolname = 'promoCode']
- Датапикер "Срок действия страхования": 
//mat-datepicker/ancestor::div[contains(@class,'mat-form-field-flex ng-tns')]
- Логотип "СБЕР СТРАХОВАНИЕ":
 //div[@class='sber-logo']
- Слайдер в блоке выбора суммы:
 //div[@class='mat-slider-wrapper']
- Хедер "Что будет застраховано?": 
//h4[@class='block-header' and .='Что будет застраховано?']
- Текстовые блоки:
  - Мебель, техника и ваши вещи:
 //div[@class='sbi-form__col-2' and .=' Мебель, техника и ваши вещи ']
  - Падение летательных аппаратов и их частей:
 //div[@class='record__label' and .='Падение летательных аппаратов и их частей']
- Колонки списка, который находится под хедером "Страховая защита включенная в программу":
  - Левая:
 //div[text()='Чрезвычайная ситуация']/ancestor::ul
  - Правая:
 //div[text()='Стихийные бедствия']/ancestor::ul




## Оформление

- кнопка «заполнить по Сбер ID»
//button/span[text()=' Заполнить по Сбер ID '] 

 - кнопка «мужской»
//button/span[text()='Мужской']
 - кнопка «женский»
//button/span[text()='Женский']

- кнопка «вернуться»
 //button/span[text()='Вернуться'] 
 - кнопка «оформить»
//button/span[text()='Оформить']
- Фамилия
//input[@formcontrolname = 'lastName']
- Имя 
//input[@formcontrolname = 'name']
- Отчество
//input[@formcontrolname = 'middleName']
- Паспорт серия
//input[@formcontrolname = 'docSeries'] 
- Номер
//input[@formcontrolname = 'docNumber']
- Кем выдан
//input[@formcontrolname = 'docIssuer']
- Код подразделения
//input[@formcontrolname = 'docDepartmentCode']
- Город или населенный пункт
//input[@formcontrolname = 'registrationCity']
- Улица
//input[@formcontrolname = 'registrationStreet']
- Дом, литера, корпус, строение
//input[@formcontrolname = 'registrationHouse']
- Кваритира
//input[@formcontrolname = 'registrationFlat']
- Телефон
//input[@formcontrolname = 'contactPhone']
- Электронная почта
//input[@formcontrolname = 'contactEmail']
- Повтор электронной почты
//input[@formcontrolname = 'repeatEmail']
- Чекбоксы:
  - Отчество отсутствует:
 //input[@id='mat-checkbox-1-input']
  - Улица отсутствует:
 //*[@id='mat-checkbox-2-input']
- Датапикеры:
  - Дата рождения: //input[@formcontrolname='birthDate']/ancestor::div[contains(@class,'mat-form-field-flex ng-tns')]
   - Дата выдачи: //input[@formcontrolname='docDepartmentCode']/ancestor::div[contains(@class,'mat-form-field-flex ng-tns')]




