# $messageInfo
Returns the message information.

## Usage
```py
$messageInfo[(Channel ID;Message ID);Param]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Channel ID | Channel ID to return this information. | False |
| Message ID | Message ID to return this information. | False |
| Param | What param of information should be returned? | True |

### Supported inputs for `Param`
| Input | Description |
| ----- | ----------- |
| author | Returns message author id. |
| id | Returns message id. |
| channel | Returns the channel ID where the message is located. |
| created | Returns the time when the message was sent. |
| content | Returns the content of the message. |
| issystem | Checks if the message is system. |
| url | Returns a reference to the message. |
| pinned | Pins the message. |
| guild | Returns the guild ID where the message is located. |
| position | Return position message. |
| type | Return type message. |