# $addReaction
Добавляет реакцию к сообщению.

## Использование
```py
$addReaction[(Channel ID;Message ID);Emoji]
```

## Парамерты
| Название | Описание | Обьязательно |
| -------- | -------- | ------------ |
| Channel ID | Айди канала где находиться сообщение. | Нет |
| Message ID | Айди сообщение где нужно поставить реакцию. | Нет |
| Emoji | Какую реакцию нужно поставить. | Да |

## Примеры
- Пример 1
```py
<Client>.add_command(name='!command', code="$addReaction[😎]")
```
- Пример 2
```py
<Client>.add_command(name='!command', code="$sendMessage[Hello!;#addReaction[👍]]")
```