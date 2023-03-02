## Онлайн чат

---
Данный проект представляет из себя онлайн чат. Весь проект реализован на языке программирования
Python без использования сторонних фреймворков или библиотек. Весь проект реализован на веб-сокетах,
доступные из библиотеки asyncio. Все данные хранятся в оперативной памяти, поэтому при перезапуске
сервера все данные будут потеряны.
---
### Запуск проекта
1. Необходимо установить Python версии 3.10 и выше
2. Установить зависимости из файла requirements.txt командой:
```python
pip install -r requirements.txt
```
3. Находясь в корневой директории проекта запустить сервер командой:
```python
python example_server.py
```
4. После запуска сервера можно установить соединение с ним с помощью клиента. Для этого необходимо запустить:
```python
python exemple_client.py
```
---
### Команды для работы с чатом
Все команды вводятся в поле ввода сообщения. Командой серверу является первое слово в сообщении.
Все команды вводятся без кавычек. Все команды вводятся на английском языке.
В случае неверного ввода команды, сервер выдаст сообщение об ошибке.
1. **help** - выводит список всех доступных команд.
2. **rename** {new_name: str} - изменяет имя пользователя на {new_name}. Имя пользователя не может
содержать пробелы или быть уже занятым.
3. **exit** - выход из чата. Разрывает соединение с сервером.
4. **users** - выводит список всех пользователей, которые находятся в чате.
5. **send** {message: str} - отправляет сообщение всем пользователям в чате. У данной команды
существуют опциональные параметры:
    1. **-u --username** {username: str} - отправляет сообщение только указанному пользователю.
    2. **-t --time** {time: int} - отправляет сообщение через указанное количество секунд.
6. **cancel**  - отменяет последнее запланированное сообщение.
7. **history** - выводит историю последних 20 сообщений в чате.
8. **report** {username: str} - позволяет отправить жалобу на пользователя. Если пользователь
наберёт более 2 жалоб, то он лишиться возможности отправлять сообщения в чат на 10 минут.
