# Chat
Многопользовательский чат, построенный на многопоточном коде

Нужно создать многопользовательский консольный чат. GUI делать не нужно. Нельзя использовать фреймворки или библиотеки которые решают задачу на 80%, но можно использовать библиотеки, которые в целом облегчают разработку, например Google Guava, Apache Commons и другие.
Для взаимодействия клиента и сервера использовать TCP сокеты. 
Нельзя использовать telnet в виде клиента.
Каждый клиент при входе вводит свое имя.  Если имя уже занято, то клиент может ввести другое имя.
Клиент может ввести сообщение, при отправке оно рассылается всем другим подключенным клиентам от его имени.
Сообщения на сервере хранятся в течении текущей сессии. Соответственно, если на сервере есть несколько сообщений, то подключившийся клиент получает 100 последних сообщений. Хранение сообщений и сессий производится в оперативной памяти, нет нужды сохранять эту информацию во внешних хранилищах.
Сервер должен выдерживать до 1000 одновременных клиентов. 1к пользователей - весьма условное значение. Основная мысль заключается в том, что нужно придумать архитектуру, которая бы выдерживала как можно больше пользовательских сессий.
Клиент может отправить на сервер произвольную команду, и в ответ получить результат выполнения (например количество подключенных клиентов). Нужно иметь возможность быстро и просто добавлять новые команды. Должна быть команда help, которая возвращает информацию по другим командам.
Чат должен быть покрыт юнит-тестами.Также нужно реализовать нагрузочное тестирование с произвольным количеством клиентов. Для этой цели можно написать ботов, на какой технологии это делать — решать тебе.
Желательно для сборки проекта использовать Maven, но можно и что-то другое. Основное требование — возможность быстро запустить результат тестового задания без исправления кода.
Один из главных параметров при оценке тестового задания — выбранная архитектура и ее реализация. В идеале архитектура должна позволять нам изменить один из компонентов системы не трогая другие, например, сетевой протокол взаимодействия клиента и сервера. Так же обращается внимание на общий стиль кода, наименование методов, классов, на их размер и суть. 
В результате выполнения задания мы должны получить законченный чат, сервер которого можно отправить на боевые сервера, а клиент раздать пользователям.
