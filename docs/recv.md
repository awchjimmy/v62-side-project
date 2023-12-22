# Recv

### 0x04 SERVERLIST_REREQUEST
You click 'Back' from character selection screen.

|hex|desc|
|----|----|
|04 00|opcode|

### 0x05 CHARLIST_REQUEST
You send a character listing request after selecting a server and a channel.

|hex|desc|
|----|----|
|05 00|opcode|
|00|server|
|01|channel|

### 0x06 SERVERSTATUS_REQUEST
You send a server status request after you selected a server.

|hex|desc|
|----|----|
|06 00|opcode|
|00 00|skip|

### 0x0B SERVERLIST_REQUEST
You send a server listing request after you entered login credentials.

|hex|desc|
|----|----|
|0B 00|opcode|

### 0x0D VIEW_ALL_CHAR
When you view all characters.

|hex|desc|
|----|----|
|0D 00|opcode|

### 0x13 CHAR_SELECT
When you select your character.

|hex|desc|
|----|----|
|13 00|opcode|
|31 75 00 00|character id|
|11 00 30 30 2D 30 43 2D 32 39 2D 32 35 2D 34 33 2D 45 39|mac address "00-0C-29-25-43-E9"|
|15 00 30 30 30 43 32 39 32 35 34 33 45 39 5F 38 30 37 37 33 46 41 38|skip "000C292543E9_80773FA8"|

### 0x14 PLAYER_LOGGEDIN
When you enter the Maple world.

|hex|desc|
|----|----|
|14 00|opcode|
|31 75 00 00|character id|
|00 00|skip|

### 0x15 CHECK_CHAR_NAME
Check if the name is available or not when you create a new character.

|hex|desc|
|----|----|
|15 00|opcode|
|09 00 61 77 63 68 6A 69 6D 6D 79|character name "awchjimmy"|

### 0x16 CREATE_CHAR
When you create a new character.

|hex|desc|
|----|----|
|16 00|opcode|
|09 00 61 77 63 68 6A 69 6D 6D 79|character name "awchjimmy"|
|20 4E 00 00|face|
|4E 75 00 00|hair|
|00 00 00 00|hair color|
|00 00 00 00|skin color|
|82 DE 0F 00|top|
|A2 2C 10 00|bottom|
|81 5B 10 00|shoes|
|F0 DD 13 00|weapon|
|00|gender|
|07|str|
|07|dex|
|06|int|
|05|luk|

### 0x1A STRANGE_DATA
Not sure. Server does not response to it.

|hex|desc|
|----|----|
|1A 00|opcode|
|01 81 E6 03 E9 00 00 00 00|skip|

### 0x1C RELOG
When you exit game and go back to login screen.

|hex|desc|
|----|----|
|1C 00|opcode|

### 0x23 CHANGE_MAP
When you enter a portal.

|hex|desc|
|----|----|
|23 00|opcode|
|01|skip|
|FF FF FF FF|target id|
|06 00 6E 65 78 74 30 30|portal name "next00"|
|4A F0 B4 00 00 00 00|skip|

### 0x24 CHANGE_CHANNEL
When you change a channel.

|hex|desc|
|----|----|
|24 00|opcode|
|00|channel|
|17 A1 3F 00|skip|

### 0x2E GENERAL_CHAT
When you speak to the public with the white bubble background.

|hex| desc            |
|----|-----------------|
|2E 00| opcode          |
|05 00 68 65 6C 6C 6F| message "hello" |
|00| show            |

### 0x5C CHANGE_MAP_SPECIAL
When you enter a portal.

|hex|desc|
|----|----|
|5C 00|opcode|
|01|skip|
|09 00 74 75 74 6F 72 69 61 6C 30|portal name "tutorial0"|
|6C 00 35 00|skip|

### 0x7B CHANGE_KEYMAP
When you change your keymap settings.

|hex|desc|
|----|----|
|7B 00|opcode|
|00 00 00 00|skip|
|02 00 00 00|num changes|
|1D 00 00 00|key (1)|
|05|type (1)|
|34 00 00 00|action (1)|
|1E 00 00 00|key (2)|
|00|type (2)|
|34 00 00 00|action (2)|

### 0xC0 PLAYER_UPDATE
Notify backend to save data.

|hex|desc|
|----|----|
|C0 00|opcode|