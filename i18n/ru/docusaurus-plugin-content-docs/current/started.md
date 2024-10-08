---
title: 'Начало'
sidebar_position: 1
---

# Установка MZscript

1. Открываем VS Code и добавляем папку с нашем проектом
2. Открываем терминал (Ctrl+Shift+`)
3. Скачиваем MZscript
```py
pip install MZscript
```

## Запуск бота

1. Создаем файл `main.py`
> Это ваш главный файл с него вы будете запускать бота
2. Пише код которой будет запускать бота
```py
from MZscript import MZClient # Импортируем класс

bot = MZClient() # Создаем обьект бота

bot.add_command( # Создание команды
    name='!help', # Название команды
    code=''' 
$sendMessage[Hi!]
'''
)

bot.run('Token bot') # Сюда токен что б запустить бота
```
> Никому не давайте токен своего бота

3. Как запустить файл?
- Метод 1:

Скачиваем расширение Python в VS Code. [Клик](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-extension-pack). Потом сверху справа у вас появиться кнопка запустить файл

- Метод 2:

Открываем терминал и пишем команду которая запустит бота:
```py
python main.py
```