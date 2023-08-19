# Windows

## Инструкция для открытия журнала событий Windows

**1 способ**

1. Нажать сочетание кнопок Win+R — должно появиться окно "Выполнить"
2. Ввести команду `eventvwr`
3. Нажать "OK"
4. Нажать на вкладку "Журналы Windows"

**2 способ**

1. Воспользоваться диспетчером задач (Ctrl+Shift+Esc)
2. Нажать по меню "Файл/новая задача"
3. Ввести команду `eventvwr`
4. Нажать "OK"
5. Нажать на вкладку "Журналы Windows"

**3 способ**

1. Открыть меню «Пуск»
2. Нажать «Панель управления»
3. Выбрать раздел «Администрирование»
4. Нажать «Просмотр событий».
5. Нажать на вкладку "Журналы Windows"

## Описание журналов: Система, Приложение, Безопасность. Информация в них.

**Система** - содержит события, записываемые системными компонентами Windows. Например, в журнале системы регистрируются сбои при загрузке драйвера или других системных компонентов в процессе загрузки системы. Типы событий, которые регистрируются компонентами системы, определены на уровне операционной системы.
**Приложение** - содержатся данные, относящиеся к работе приложений и программ. Например, программа управления базой данных может зарегистрировать событие о файловой ошибке в журнале приложений. События, регистрируемые в журнале приложений, определяются разработчиками соответствующих приложений.
**Безопасность** - содержит такие события, как успешные и неуспешные попытки входа в систему, а также события, относящиеся к использованию ресурсов, такие как создание, открытие и удаление файлов и других объектов. Администраторы могут выбрать события, которые следует заносить в журнал безопасности. Например, если включен аудит входа в систему, сведения обо всех попытках входа в систему заносятся в журнал безопасности.

## Какая команда в cmd отображает текущую таблицу ARP для всех интерфейсов, присутcтвующих на компьютере?

`arp /a`
## Какая команда в cmd поможет вывести список установленных драйверов устройств?

`driverquery`

# MacOC

## Что такое логи (журнал сервера) в Linux.

Лог-файлы (файлы регистрации, журнальные файлы) на Linux - это текстовые файлы о событиях, произошедших на сайте: информация о параметрах посещений сайта и ошибках, которые возникали на нем.

| ВОПРОС | ОТВЕТ |
| ------ | ------ |
| В каком файле смотреть логи неудачных попыток авторизации | log или /var/log/secure |
| Что делает команда ls /var/log | lastlog выводит информацию о входах в систему, содержащуюся в файле **/var/log/lastlog**. |
| Какой командой посмотреть логи журнала сообщений от ядра в реальном времени?| **tail -f /var/log/syslog** позволит наблюдать запись логов в реальном времени |
| Какая команда покажет, кто из пользователей сейчас залогинен в системе и когда он зашел? | Who |
| Какая команда дает понять, когда пользователь заходил в систему и сколько времени в ней находился? | Чтобы просмотреть историю всех успешных входов в систему, просто используйте команду **last** |

## В каком файле смотреть логи неудачных попыток авторизации?

**log** или **/var/log/secure** — информация об авторизации пользователей, включая удачные и неудачные попытки входа в систему, а также задействованные механизмы аутентификации.

## Что делает команда ls /var/log?

lastlog выводит информацию (имя пользователя, порт и дату последнего входа) о входах в систему, содержащуюся в файле **/var/log/lastlog**. По умолчанию строки выводятся в том же порядке, в котором они указаны в **/etc/passwd**.

## Какой командой посмотреть логи журнала сообщений от ядра в реальном времени?

Команда **tail -f /var/log/syslog** позволит наблюдать запись логов в реальном времени.

## Какая команда покажет, кто из пользователей сейчас залогинен в системе и когда он зашел?

Who

## Какая команда дает понять, когда пользователь заходил в систему и сколько времени в ней находился?

Чтобы просмотреть историю всех успешных входов в систему, просто используйте команду **last**. 

Вывод должен выглядеть следующим образом. Как видите, в нем перечислены пользователи, IP-адрес, с которого пользователь получил доступ к системе, дата и время входа в систему.