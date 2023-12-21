# Recv

### CHARLIST_REQUEST
You send a character listing request after selecting a server and a channel.

|hex|desc|
|----|----|
|05 00|opcode|
|00|server|
|01|channel|

### SERVERSTATUS_REQUEST
You send a server status request after you selected a server.

|hex|desc|
|----|----|
|06 00|opcode|
|00 00|skip|

### SERVERLIST_REQUEST
You send a server listing request after you entered login credentials.

|hex|desc|
|----|----|
|0B 00|opcode|

### CHAR_SELECT
When you select your character.

|hex|desc|
|----|----|
|13 00|opcode|
|31 75 00 00|character id|
|11 00 30 30 2D 30 43 2D 32 39 2D 32 35 2D 34 33 2D 45 39|mac address "00-0C-29-25-43-E9"|
|15 00 30 30 30 43 32 39 32 35 34 33 45 39 5F 38 30 37 37 33 46 41 38|skip "000C292543E9_80773FA8"|

### PLAYER_LOGGEDIN
When you enter the Maple world.

|hex|desc|
|----|----|
|14 00|opcode
|31 75 00 00|character id|
|00 00|skip|

### RELOG
When you exit game and go back to login screen.

|hex|desc|
|----|----|
|1C 00|opcode|

### CHANGE_MAP
When you enter a portal.

|hex|desc|
|----|----|
|23 00|opcode|
|01|skip|
|FF FF FF FF|target id|
|06 00 6E 65 78 74 30 30|portal name "next00"|
|4A F0 B4 00 00 00 00|skip|

### CHANGE_CHANNEL
When you change a channel.

|hex|desc|
|----|----|
|24 00|opcode|
|00|channel|
|17 A1 3F 00|skip|

### GENERAL_CHAT
When you speak to the public with the white bubble background.

|hex| desc            |
|----|-----------------|
|2E 00| opcode          |
|05 00 68 65 6C 6C 6F| message "hello" |
|00| show            |

### CHANGE_MAP_SPECIAL
When you enter a portal.

|hex|desc|
|----|----|
|5C 00|opcode|
|01|skip|
|09 00 74 75 74 6F 72 69 61 6C 30|portal name "tutorial0"|
|6C 00 35 00|skip|

### PLAYER_UPDATE
Notify backend to save data.

|hex|desc|
|----|----|
|C0 00|opcode|