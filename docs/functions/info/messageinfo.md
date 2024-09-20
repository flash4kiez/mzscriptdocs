# $messageInfo
Returns the message information.

## Usage
```py
$messageInfo[(Channel ID; Message ID);Type]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Channel ID | Guild ID to return this information. | False |
| Message ID | User ID to return this information. | False |
| Type | What type of information should be returned? | True |

### Supported inputs for `Type`
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
| position |  |
| type | |