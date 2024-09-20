# $channelInfo
Returns the channel information.

## Usage
```py
$channelInfo[(Channel ID);Param]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Channel ID | Channel ID to return this information. | False |
| Param | What param of information should be returned? | True |

### Supported inputs for `Param`
| Input | Description |
| ----- | ----------- |
| category | The parent ID of channel. |
| created | When channel was created. (unix-time) |
| guild | Where is channel located. |
| name | Channel name. |
| id | Channel ID. |
| type | Channel type. |
| position | The channel position in channel list. |
| last_message | The last message id in channel. |
| nsfw | "true" if the channel is a NSFW and "false" if isn't. |
| slowmode_delay | Channel slowmode. |
| thread_slowmode | Tread-channel slowmode. |
| auto_archive_duration | The thread archive duration time. |
| topic | The topic of channel. |
| bitrate | The bitrate of voice channel. |
| user_limit | Returns the max users available to join in voice channel. |
| region | The region of voice channel. |