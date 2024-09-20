# $botInfo
Returns the bot information.

## Usage
```py
$botInfo[Type]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Type | What type of information should be returned? | True |

### Supported inputs for `Type`
| Input | Description |
| ----- | ----------- |
| is_private | Returns whether the bot is private |
| image |  |
| description | Returns the description of the bot. |
| icon | Returns the bots avatar. |
| id | Returns the bot ID. |
| name | Returns the bot name. |
| owner | Returns the bot creator's ID. |
| guilds | Returns a list of guilds. |
| users | Returns a list of users. |
| ping | Returns the bot ping. |