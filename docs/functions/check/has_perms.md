# $hasPerms
Cheking if the user has a permissions.

## Usage
```py
$hasPerms[(Guild ID;User ID);Permission]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Guild ID | Guild ID the user is in. | False |
| User ID | User ID to check for permissions. | False |
| Permission | Permissions that will be checked. | True |

### Supported inputs for `Permission`
| Input | Description |
| ----- | ----------- |
| add_reactions | Returns True if a user can add reactions to messages. |
| admin | Returns True if a user is an administrator. This role overrides all other permissions. |
| attach_files | Returns True if a user can send files in their messages. |
| ban_members | Returns True if a user can ban users from the guild. |
| change_nickname | Returns True if a user can change their nickname in the guild. |
| connect | Returns True if a user can connect to a voice channel. |
| create_forum_threads | Returns True if a user can create threads in forum channels. |
| create_instant_invite | Returns True if the user can create instant invites. |
| create_private_threads | Returns True if a user can create private threads. |
| create_public_threads | Returns True if a user can create public threads. |
| deafen_members | Returns True if a user can deafen other users. |
| embed_links | Returns True if a user’s messages will automatically be embedded by Discord. |
| external_emojis | Returns True if a user can use emojis from other guilds. |
| external_stickers | Returns True if a user can use stickers from other guilds. |
| kick_members | Returns True if the user can kick users from the guild. |
| manage_channels | Returns True if a user can edit, delete, or create channels in the guild. |
| manage_emojis | Returns True if a user can create, edit, or delete emojis. |
| manage_emojis_and_stickers | Returns True if a user can create, edit, or delete emojis, stickers. |
| manage_events | Returns True if a user can manage guild events. |
| manage_guild | Returns True if a user can edit guild properties. |
| manage_guild_expressions | Returns True if a user can create, edit, or delete emojis, stickers, and soundboard sounds. |
| manage_messages | Returns True if a user can delete or pin messages in a text channel. |
| manage_nicknames | Returns True if a user can change other user’s nickname in the guild. |
| manage_permissions | An alias for `manage_roles`.  |
| manage_roles | Returns True if a user can create or edit roles less than their role’s position. |
| manage_threads | Returns True if a user can manage threads. |
| manage_webhooks | Returns True if a user can create, edit, or delete webhooks. |
| mention_everyone | Returns True if a user’s @everyone or @here will mention everyone in the text channel. |
| moderate_members | Returns True if a user can perform limited moderation actions, such as timeouts or editing members’ flags. |
| move_members | Returns True if a user can move users between other voice channels. |
| mute_members | Returns True if a user can mute other users. |
| priority_speaker | Returns True if a user can be more easily heard while talking. |
| read_message_history | Returns True if a user can read a text channel’s previous messages. |
| read_messages | Returns True if a user can read messages in channel. |
| request_to_speak | Returns True if a user can request to speak in a stage channel. |
| send_messages | Returns True if a user can send messages from all or specific text channels and create threads in forum channels. |
| send_messages_in_threads | Returns True if a user can send messages in threads. |
| send_tts_messages | Returns True if a user can send TTS messages from all or specific text channels. |
| send_voice_messages | Returns True if a user can send voice messages. |
| speak | Returns True if a user can speak in a voice channel. |
| start_embedded_activities | An alias for `use_embedded_activities`. |
| stream | Returns True if a user can stream in a voice channel. |
| use_application_commands | Returns True if a user can use application commands. |
| use_embedded_activities | Returns True if a user can use activities (applications with the embedded flag) in a voice channel. |
| use_external_emojis | Returns True if a user can use emojis from other guilds. |
| use_external_sounds | Returns True if a user can use custom soundboard sounds from other guilds. |
| use_external_stickers | Returns True if a user can use stickers from other guilds. |
| use_slash_commands | Returns True if a user can use slash commands. |
| use_soundboard | Returns True if a user can use the soundboard in voice channels. |
| use_voice_activation | Returns True if a user can use voice activation in voice channels. |
| value | The raw value. This value is a bit array field of a 53-bit integer representing the currently available permissions. You should query permissions via the properties rather than using this raw value. |
| view_audit_log | Returns True if a user can view the guild’s audit log. |
| view_channel | Returns True if a user can view all or specific channels. |
| view_creator_monetization_analytics | Returns True if a user can view role subscription insights. |
| view_guild_insights | Returns True if a user can view the guild’s insights. |