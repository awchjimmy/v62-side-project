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

### PLAYER_LOGGEDIN
When you entered the Maple world.

|hex|desc|
|----|----|
|14 00|opcode
|31 75 00 00|character id|
|00 00|skip|

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

|hex|desc|
|----|----|
|2E 00|opcode|
|05 00 68 65 6C 6C 6F|mapleAsciiString "hello"|
|00|show|
