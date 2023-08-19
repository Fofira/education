Изучите существующие алгоритмы балансировки нагрузки. Создайте файл exercise1.md и опишите изученные алгоритмы, указав их особенности и недостатки.

# Алгоритмы балансировки нагрузки
указав их особенности и недостатки.

**Алгоритм балансировки нагрузки** – это набор правил, которым следует балансировщик нагрузки для определения наилучшего сервера для каждого из различных клиентских запросов. Алгоритмы балансировки нагрузки делятся на две основные категории.
Существует много различных алгоритмов и методов балансировки нагрузки. Выбирая конкретный алгоритм, нужно исходить, во-первых, из специфики конкретного проекта, а во-вторых — из целей. которые мы планируем достичь.
**В числе целей, для достижения которых используется балансировка, нужно выделить следующие:**
- справедливость: нужно гарантировать, чтобы на обработку каждого запроса выделялись системные ресурсы и не допустить возникновения ситуаций, когда один запрос обрабатывается, а все остальные ждут своей очереди;
- эффективность: все серверы, которые обрабатывают запросы, должны быть заняты на 100%; желательно не допускать ситуации, когда один из серверов простаивает в ожидании запросов на обработку (сразу же оговоримся, что в реальной практике эта цель достигается далеко не всегда);
- сокращение времени выполнения запроса: нужно обеспечить минимальное время между началом обработки запроса (или его постановкой в очередь на обработку) и его завершения;
- сокращение времени отклика: нужно минимизировать время ответа на запрос пользователя.
Очень желательно также, чтобы алгоритм балансировки обладал следующими свойствами:
- предсказуемость: нужно чётко понимать, в каких ситуациях и при каких нагрузках алгоритм будет эффективным для решения поставленных задач;
- равномерная загрузка ресурсов системы;
- масштабирумость: алгоритм должен сохранять работоспособность при увеличении нагрузки.

## Round Robin
Round Robin, или алгоритм кругового обслуживания, представляет собой перебор по круговому циклу: первый запрос передаётся одному серверу, затем следующий запрос передаётся другому и так до достижения последнего сервера, а затем всё начинается сначала.
Самой распространёной имплементацией этого алгоритма является, конечно же, метод балансировки Round Robin DNS. Как известно, любой DNS-сервер хранит пару «имя хоста — IP-адрес» для каждой машины в определённом домене. Этот список может выглядеть, например, так:
```
example.com	xxx.xxx.xxx.2
www.example.com	xxx.xxx.xxx.3
```
С каждым именем из списка можно ассоциировать несколько IP-адресов:
```
xample.com	xxx.xxx.xxx.2
www.example.com	xxx.xxx.xxx.3
www.example.com	xxx.xxx.xxx.4
www.example.com	xxx.xxx.xxx.5
www.example.com	xxx.xxx.xxx.6
```
DNS-сервер проходит по всем записям таблицы и отдаёт на каждый новый запрос следующий IP-адрес: например, на первый запрос — xxx.xxx.xxx.2, на второй — ххх.ххх.ххх.3, и так далее. В результате все серверы в кластере получают одинаковое количество запросов.
В числе несомненных **плюсов** этого алгоритма следует назвать:
- во-первых, независимость от протокола высокого уровня. Для работы по алгоритму Round Robin используется любой протокол, в котором обращение к серверу идёт по имени.
- Балансировка на основе алгоритма Round Robin никак не зависит от нагрузки на сервер: кэширующие DNS-серверы помогут справиться с любым наплывом клиентов.
- Использование алгоритма Round Robin не требует связи между серверами, поэтому он может использоваться как для локальной, так и для глобальной балансировки,.
- Наконец, решения на базе алгоритма Round Robin отличаются низкой стоимостью: чтобы они начали работать, достаточно просто добавить несколько записей в DNS.
Алгоритм Round Robin имеет и целый ряд существенных **недостатков**.
- Чтобы распределение нагрузки по этому алгоритму отвечало упомянутым выше критериями справедливости и эффективности, нужно, чтобы у каждого сервера был в наличии одинаковый набор ресурсов. При выполнении всех операций также должно быть задействовано одинаковое количество ресурсов. В реальной практике эти условия в большинстве случаев оказываются невыполнимыми.
- Также при балансировке по алгоритму Round Robin совершенно не учитывается загруженность того или иного сервера в составе кластера. Представим себе следующую гипотетическую ситуацию: один из узлов загружен на 100%, в то время как другие — всего на 10 — 15%. Алгоритм Round Robin возможности возникновения такой ситуации не учитывает в принципе, поэтому перегруженный узел все равно будет получать запросы. Ни о какой справедливости, эффективности и предсказуемости в таком случае не может быть и речи.
- В предыдущем разделе мы перечислили основные недостатки алгоритма Round Robin. Назовём ещё один: в нём совершенно не учитывается количество активных на данный момент подключений.
Рассмотрим практический пример. Имеется два сервера — обозначим их условно как А и Б. К серверу А подключено меньше пользователей, чем к серверу Б. При этом сервер А оказывается более перегруженным. Как это возможно? Ответ достаточно прост: подключения к серверу А поддерживаются в течение более долгого времени по сравнению с подключениями к серверу Б.
В силу описанных выше обстоятельств сфера применения алгоритма Round Robin весьма ограничена.
## Weighted Round Robin
Это — усовершенствованная версия алгоритма Round Robin. Суть усовершенствований заключается в следующем: каждому серверу присваивается весовой коэффициент в соответствии с его производительностью и мощностью. Это помогает распределять нагрузку более гибко: серверы с большим весом обрабатывают больше запросов. Однако всех проблем с отказоустойчивостью это отнюдь не решает. Более эффективную балансировку обеспечивают другие методы, в которых при планировании и распределении нагрузки учитывается большее количество параметров.
## Least Connections
Описанную проблему можно решить с помощью алгоритма, известного под названием least connections (сокращённо — leastconn). Он учитывает количество подключений, поддерживаемых серверами в текущий момент времени. Каждый следующий вопрос передаётся серверу с наименьшим количеством активных подключений.
## Weighted Least Connections
Существует усовершенствованный вариант этого алгоритма, предназначенный в первую очередь для использования в кластерах, состоящих из серверов с разными техническими характеристиками и разной производительностью. Он называется **Weighted Least Connections** и учитывает при распределении нагрузки не только количество активных подключений, но и весовой коэффициент серверов.
В числе других усовершенствованных вариантов алгоритма Least Connections следует прежде всего выделить **Locality-Based Least Connection Scheduling** и **Locality-Based Least Connection Scheduling with Replication Scheduling**.
## Locality-Based Least Connection Scheduling
Первый метод был создан специально для кэширующих прокси-серверов. Его суть заключается в следующем: наибольшее количество запросов передаётся серверам с наименьшим количеством активных подключений. За каждым из клиентских серверов закрепляется группа клиентских IP. Запросы с этих IP направляются на «родной» сервер, если он не загружен полностью. В противном случае запрос будет перенаправлен на другой сервер (он должен быть загружен менее чем наполовину).
## Locality-Based Least Connection Scheduling with Replication Scheduling
В алгоритме Locality-Based Least Connection Scheduling with Replication Scheduling каждый IP-адрес или группа IP-адресов закрепляется не за отдельным сервером, а за целой группой серверов. Запрос передаётся наименее загруженному серверу из группы. Если же все серверы из «родной» группы перегружены, то будет зарезервирован новый сервер. Этот новый сервер будет добавлен к группе, обслуживающей IP, с которого был отправлен запрос. В свою очередь наиболее загруженный сервер из этой группы будет удалён — это позволяет избежать избыточной репликации.
## Destination Hash Scheduling
Алгоритм Destination Hash Scheduling был создан для работы с кластером кэширующих прокси-серверов, но он часто используется и в других случаях. В этом алгоритме сервер, обрабатывающий запрос, выбирается из статической таблицы по IP-адресу получателя.
## Source Hash Scheduling
Алгоритм Source Hash Scheduling основывается на тех же самых принципах, что и предыдущий, только сервер, который будет обрабатывать запрос, выбирается из таблицы по IP-адресу отправителя.
## Sticky Sessions
Sticky Sessions — алгоритм распределения входящих запросов, при котором соединения передаются на один и тот же сервер группы. Он используется, например, в веб-сервере Nginx. Сессии пользователя могут быть закреплены за конкретным сервером с помощью метода IP hash (подробную информацию о нём см. в официальной документации). С помощью этого метода запросы распределяются по серверам на основе IP-aдреса клиента. Как указано в документации, «метод гарантирует, что запросы одного и того же клиента будет передаваться на один и тот же сервер». Если закреплённый за конкретным адресом сервер недоступен, запрос будет перенаправлен на другой сервер.
Пример фрагмента конфигурационного файла:
```
upstream backend {
ip_hash;

server backend1.example.com;
server backend2.example.com;
server backend3.example.com;
server backend4.example.com;
}
```
Начиная с версии 1.2.2 в Nginx для каждого сервера можно указывать вес.
Применение этого метода сопряжено с некоторыми проблемами. Проблемы с привязкой сессий могут возникнуть, если клиент использует динамический IP. В ситуации, когда большое количество запросов проходит через один прокси-сервер, балансировку вряд ли можно назвать эффективной и справедливой. Описанные проблемы, однако, можно решить, используя cookies. В коммерческой версии Nginx имеется специальный модуль sticky, который как раз использует cookies для балансировки. Есть у него и бесплатные аналоги — например, nginx-sticky-module.
Можно использовать метод sticky-sessions и в HAProxy.