|Command        |Aliases|Arguments|Description|Example(s)|
|---------------|-------|---------|-----------|----------|
/adddj          |/queue  |`@username  userID` |If the given user is not on the waitlist, adds them to the waitlist.   |     
/addstaff       |        |`role#` `@username  userID` |Adds a user to the staff with the given role.   |`/addstaff 2 @new_bouncer`  
/ban            |        |`reason#` `duration` `@username userID` |Bans a user in the room with given username or userID, reason# and duration.    |`/ban 1 h @baduser`, `/ban 4 f 1234567` 
/bandurations   |/bd     |            |Displays a list of valid ban durations to be used with **/ban**.     |
/banlist        |        |            |Retrieves the room's banlist and displays it. Debug purposes.      |     
/banlist        |        |            |Downloads the ban list and saves it to data/banList_(roomslug).txt. Will overwrite.      |
/banreasons     |/br     |            |Displays a list of valid ban reasons to be used with **/ban**.     |
/clear          |/cls    |            |Clears screen.      |
/commands       |/cmds   |            |Lists active and inactive chat commands, also shows the link to this file.     |     
/cycle          |        |`[on     off]`  |Displays current waitlist cycle status. If **on** is given, turns cycle ON. If **off**, turns cycle OFF.    |`/cycle on`, `/cycle off`   
/dc             |        |            |Displays a raw list of users' IDs that have recently disconnected while on the waitlist, with their previous position and time they disconnected. Used for debugging.     |      
/deletemsg      |/delmsg, /dm    |`chatID`    |Deletes a chat message with the given chatID. Looks something like **0123456-1234567890123**    |`/dm 1234567-1417172092351`     
/description    |        |`[set]`     |If "set" is not specified, displays room's current description. Otherwise, changes the description to whatever is typed after "set". Use \n for newlines.       |    
/disable        |        |`name of a chat command`    |Deactivates a given chat command.   |`/disable 8ball`        
/enable         |        |`name of a chat command`    |Activates a given chat command. |`/enable roll`      
/exit           |/quit   |            |**Safely closes the program. Important.**           |
/friend         |/f      |`add    a` `userID` |Sends a friend request to the given userID. If that userID sent you a request first, accepts the request instead. Subject to removal since the friends list system is trivial for a bot.        |
/getuser        |/showuser, /user    |`username   userID` |If user is in the room, displays info about the given user. If no argument, returns your own info.  |`/user`, `/user someoneinroom`, `/user 1234567` 
/grab           |/g      |            |Grabs song into the currently active playlist.         | 
/home           |        |            |Joins HOME room defined in coreoptions.         |
/join           |/j, /room, /r   |`room slug` |Joins the given room. A **room slug** is what can be found at the end of a room's URL. (e.g. https://plug.dj/this-is-the-room-slug) |`/j this-is-the-room-slug`     
/kick           |        |`reason#` `@username    userID` |Bans a user in the room with given username or userID and reason#, then unbans them 2.5 seconds later.  `/kick 2 @username`, |`/kick 5 1234567`  
/link           |        |            |Displays link of current song.          |
/listsettings   |        |            |Displays a list of BotSettings options and their current values.           | 
/loadblacklists |        |            |Reloads blacklists from their respective json files. Can be used after editing a blacklist with a text editor.          |
/me             |        |`*any text*`    |Default /me behavior on plug.dj.    |`/me hello`     
/meh            |/m      |            |Meh.            |
/movedj         |        |`position#` `@username  userID` |If the user given is on the waitlist, moves the given user to the given position #.     |
/mute           |        |`reason#` `duration` `@username userID` |Mutes a user in the room with given username or userID, reason# and duration.   |`/mute 3 s @user`, `/mute 2 m 1234567`  `/wl lock clear`, `/wl unlock`, `/wl j`, `/wl l`
/mutedurations  |/md     |            |Displays a list of valid mute durations to be used with **/mute**.          |
/mutereasons    |/mr     |            |Displays a list of valid mute reasons to be used with **/mute**.            |
/playlist       |/pl     |            |Displays name of currently active playlist.         |
/reloadsettings |/rs     |            |Loads settings.json         |
/removestaff    |/rmstaff    |`@username  userID` |Removes a user with the given username or userID from the room's staff. |`/rmstaff 1234567`, `/rmstaff @userinroom`  
/roles          |        |            |Displays a list of valid role values for use with **/addstaff**.            |
/saveseen       |/ss     |            |Writes current data of seen users to data/seenUsers.json            |
/set            |        |`<name of BotSettings option>` `<value to set>` |Changes the value of a given BotSettings option, if valid.  |`/set timestampColor cyan`, `/set welcomeusers true`        
/setplaylist    |/setpl  |`playlistID`    |Activates a playlist **on your account** with the given playlistID. |`/setpl 45678901`       
/skip           |        |`<t,r,o,l,s>`     |Skips the current song with a predefined reason. T=Theme,R=RepeatOffender,O=OP,L=Language,S=Sound. All options but R will bring the DJ back up the list.   | `/skip s`
/stafflist      |        |            |Downloads the staff list and saves it to data/staffList_(roomslug).txt. Will overwrite.         |
/syncusers      |        |            |Gets the list of users from the server. Should only be used if the userlist screws up or has "unavailable" users, which it shouldn't.        |   
/trigger        |        |`[trigger char]`    |Displays current trigger. If valid argument is given, sets the trigger to given argument.   |`/trigger $`        
/unban          |        |`userID`    |Unbans user with the given userID.  |`/unban 1234567`        
/unmute         |        |`@username  userID`     |Unmutes a user with the given username or userID.   |`/unmute 1234567`, `/unmute @userinroom`    
/unqueue        |/undj, /removedj, /rmdj |`@username  userID` |Removes a user with the given username or userID from the waitlist. |`/rmdj 1234567` 
/update         |        |            |Grabs version.json within the git repo, and compares it against the current bot version.            |
/userlist       |/users, /u  |        |Displays the userlist, and amount of guests if any.         |
/votes          |/v      |            |Displays the current woot/grab/meh vote count.          |
/waitlist       |/djlist, /djs, /wl  |`[join  j, leave    l, lock, unlock]` `[clear (if lock)]`   |If no argument, displays the waitlist and its lock/cycle status. join: joins waitlist. leave: leaves waitlist. lock: locks waitlist; if **clear** is given, clears waitlist too. unlock: unlocks waitlist.  |
/welcome        |        |`[set]`     |If "set" is not specified, displays room's current welcome message. Otherwise, changes the welcome message to whatever is typed after "set".        |    
/woot           |/w      |            |Woot.       |    
/writeplaylists |        |            |Retrieves a list of playlists on your account and saves it to data/playlists.json. Used for debug purposes.         |
