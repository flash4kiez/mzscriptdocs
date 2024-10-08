---
title: 'Команды бота'
sidebar_position: 1
---

# Команды

Команда в MZscript выглядит примерно так
```py
bot.add_command(
    name='!help',
    code='''
$sendMessage[Hello World!]    
'''
)
```
Бот отправит в канал `Hello World!`

## Псевдонимы

Если вы хотите создать псевдонимы команде

Вам надо вынести свой код в переменую

И потом добавить ее в `<CLient>.add_command()`

`main.py`
```py
code = '''
$sendMessage[Hi!]
'''

bot.add_command(name='!hi', code=code)
bot.add_command(name='!hello', code=code)
```

Примерно так работают псевдонимы в MZscript

Тоже самое можно использовать в когах

## Коги
Если вы не хотите держать все команды в `main.py` вам нужны `коги`

`Коги` вам загрузить любую папку с файлами или сам файл

### Загрузка папки

В `main.py` пишем функцию которая загрузит папку

```py
bot.load_commands('cogs') # Можна любое имя задать папке
```
> Самое главное, создайте папку

Ваша структура проекта должна быть примерно такой:
```
mybot
├── cogs
│   └── hello.py
└── main.py
```

Теперь в `hello.py` пишем команду

```py
from MZscript import MZClient
# import and set client argument to MZClient is not nessecary

# but gives you code highlighting
def setup(client: MZClient):
    client.add_command(
    name="!command",
    code="""
$sendMessage[Hello!]
""")

    client.add_command(
    name="!command2",
    code="""
$sendMessage[Hello 2!]
""")
```

Примерно так выглядит ког в MZscript

Вы можите в папке создать много файлов

Но если вы хотите создать папку в папке вам надо использовать другую функцию

### Загрузка файла

Допустим, ваша структура проекта выглядит так
```
mybot
├── cogs
│   ├── utils
│   │   └── hello.py
│   └── moderation
│   │   └── ban.py
└── main.py
```

Вам нужно команда которая загрузит каждый файл

```py
bot.load_command('cogs.utils.hello')
```
В случае `hello.py` нам нужно прописать такой путь

Что б не писать много раз `<Client>.load_command()` мы можем написать загрузчик файлов

Вам нужен модуль `os`. Он по умолчанию есть в Python

`main.py`
```py
from MZscript import MZClient
import os # Модуль для работы файлов

# Самой загрузчик
for folder in os.listdir('cogs'): # Получаем все что есть в папке cogs
    for file in os.listdir(f'cogs/{folder}'): # Теперь получаем все что есть в папках
        if file.endswith('.py'): # Работает только с .py файлами
            bot.load_command(f'cogs.{folder}.{file[:-3]}') # Загружаем файлы

bot.run('Token bot')
```

Теперь ваши файлы с папки `cogs` загруженны