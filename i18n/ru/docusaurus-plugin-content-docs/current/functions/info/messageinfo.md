# $messageInfo
Returns the message information.

## Использование
```py
$messageInfo[(Channel ID;Message ID);Param]
```

## Параметры
| Название | Описание | Обьязательно |
| -------- | -------- | ------------ |
| Channel ID | Айди канала где есть сообщения. | Нет |
| Message ID | Айди сообщения. | Нет |
| Param | Какой тип информации вернуть? | Да |

### Информацию которую можно вернуть:
| Название | Описание |
| -------- | -------- |
| author | Возвращает айди автора сообщения. |
| id | Возвращает айди сообщения. |
| channel | Возвращает айди канала где есть сообщения. |
| created | Возвращает время когда было отправлено сообщения. |
| content | Возвращает содержимое сообщения. |
| issystem | Проверяет есть ли сообщения системным. |
| url | Возвращает ссылку на сообщения. |
| pinned | Прикрепляет сообщения. |
| guild | Возвращает айди гильдии где есть сообщения. |
| position | Возвращает позицию сообщения. |
| type | Возвращает тип сообщения. |