---
title: Commands
---
# Commands
Here there are guides or explanations for every command that Tickety has.

## General Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -help | Show the help menu | [click](#help-command) |
| -about | Get to know me :smirk: | [click](#about-command) |

## User Ticket Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -new | Create a new ticket | [click](#new-ticket-command) |
| -close | Close the ticket you're currently in | [click](#close-ticket-command) |
| -add | Add a user to a ticket | [click](#add-to-ticket-command) |
| -info | Get the info of a ticket | [click](#info-command) |

## Admin Ticket Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -rename | Rename a ticket | [click](#rename-ticket-command) |
| -transcript | Get the transcript of a ticket, in html or txt format | [click](#transcript-command) |
| -forceclose | Force close a bugged ticket | [click](#force-close-command) |

## Moderation Commands
::: warning
If you would like to disable these commands for your admins, please see [this command](#setmoderation).
:::

| Command | Description | Guide |
| ------- | ----------- | ----- |
| -blacklist | Block this user from performing Tickety commands | [click](#blacklist-command) |
| -unblacklist | Allow this user to perform Tickety commands again. | [click](#unblacklist-command) |
| -blacklists | View all blacklists for this server | [click](#blacklists-command) |
| -kick | Kick a user from the server | [click](#kick-command) |
| -ban | Ban a user from the server | [click](#ban-command) |
| -mute | Mute a user on the server | [click](#mute-command) |

## Configuration Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -setlog | Set the logging channel | [click](#set-log-command) |
| -setcategory | Set the category tickets will be created in | [click](#set-category-command) |
| -setopen | Determine if you want users to be able to open tickets | [click](#set-open-command) |
| -settranscriptslog | Set the log all transcripts will be sent in | [click](#set-transcripts-log-command) |
| -setmaxtickets | Set the amount of tickets one user can have | [click](#set-max-tickets-command) |
| -setmoderation | Enable/disable the Tickety moderation commands | [click](#set-moderation-command)
| -setmsg | Set the welcome message for new tickets | [click](#set-message-command) |
| -setprefix | Set the command prefix | [click](#set-prefix-command) |
| -setrole | Set the admin role | [click](#set-role-command) |
| -redeem | Redeem a premium token on this server | [click](#redeem-premium-command) |

## Command Guides
### Help Command
```
-help
```
The help command shows all the commands in a neat message. It will only show the admin commands to users that have the admin role.

### About Command
```
-about
```
The about command shows a message to the user explaining what Tickety does, also it displays some neat statistics about Tickety.
Like the amount of users and servers Tickety has. It also shows an explaining message about Premium.

### New Ticket Command
```
-new [@user] [subject]
```
This command creates a new ticket for the executing user. Admins can tag a user as the first argument to include that person into the newly created ticket.
All words after the command that are not a tag of a user will be set as the subject of the ticket.

Example: `-new @Stan#8888 I need help regarding Tickety`

### Close Ticket Command
```
-close [reason]
```
This command can only be executed in a ticket channel. When no reason is provided it will ask for a confirmation, 
once the closing has been confirmed it will close the ticket and send a message in the ticket log (if set), and
will send the transcript in the transcript log (if set).

If a reason is provided it will instantly close the ticket and add the reason to the message in the ticket log.

### Add To Ticket Command
```
-add <@user> [#channel]
```
This command can add users to a ticket channel. 
When executed in a ticket channel you will have to provide the user ID as the first argument.
When executed outside a ticket channel you can mention the user as first argument, and mention the channel as the second argument.
 
Example inside ticket: `-add 352854019934257156`
Example outside of ticket: `-add @Stan#8888 #ticket-0001`
 
### Info Command
```
-info
```
This command can only be executed inside a ticket channel. It will give basic information about a ticket.
It will return the creator of the ticket, the date of creation, the ticket id and the subject of the ticket.

### Rename Ticket Command
```
-rename <name>
```
This command can only be executed inside a ticket channel. It will rename the ticket to the given name.

Example: `-rename report`, will rename a ticket called `ticket-0001` to `report-0001`.

### Transcript Command
```
-transcript [html/txt]
```
This command can only be executed inside a ticket channel. It will send a transcript of the full conversation.
You can either give `html` or `txt` as argument, which respectively return a html version or a text version of the transcript.
When no argument is provided a html document will be returned.

Example: `-transcript txt`

### Force Close Command
```
-forceclose
```
This command can be used in a ticket channel that won't close using the -close command. 
For this command to work the channel name has to start with `ticket-`.

### Blacklist Command
```
-blacklist <@user>
```
When a user is spamming/abusing tickets, you may want to block him from opening tickets. You can do this with the blacklist command.
It will prevent the user from using **any** Tickety commands.

Example: `-blacklist @Stan#8888`

### Unblacklist Command
```
-unblacklist <@user>
```
If a blacklisted user has shown good behaviour you can unblacklist him, to allow him to open tickets again.

Example: `-unblacklist @Stan#8888`

### Blacklists Command
```
-blacklists
```
This command shows a list of all the users you have blacklisted in your server.

### Kick Commaand
```
-kick <@user> [reason]
```
With this command you can kick users from your discord server. Add a reason if necessary.

Example: `-kick @Stan#8888 This user has been advertising.`

### Ban Command
```
-ban <@user> [reason]
```
With this command you can ban users from your discord server. Add a reason if necessary.

Example: `-ban @Stan#8888 This user has been advertising repeatedly.`

### Mute Command
```
-mute <@user>
```
With this command you can mute a user from your discord server. They will get the `Muted` role applied to them and won't be able to speak in any channels.  
To unmute simply remove the role

Example: `-mute @Stan#8888`

### Set Log Command
```
-setlog [#channel/disable]
```
With this command you can set the channel in which the ticket log messages will be sent. To disable the ticket log just put `disable` as the channel

Example to set a channel: `-setlog #tickets-log`
Example to disable log: `-setlog disable`

### Set Category Command
```
-setcategory <name>
```
With this command you can set the category that tickets will be created in.

Example: `-setcategory tickets`

### Set Open Command
```
-setopen <true/false>
```
With this command you can determine whether or not users should be able to open tickets. This is useful for when you're being raided, or when your support team is inactive/offline.

Example: `-setopen true`

### Set Transcripts Log Command
```
-settranscriptslog [#channel/disable[
```
With this command you can set the channel in which all the transcripts will be sent. To disable the transcript log just put `disable` as the channel

::: warning
You generally want this channel to not be public to all users, because all transcripts will be sent here.
:::

Example to set a channel: `-settranscriptslog #transcripts-log`
Example to disable log: `-settranscriptslog disable`

### Set Max Tickets Command
``` 
-setmaxtickets <amount>
```
Set the maximum amount of tickets that one user can have in your server. Has to range between 1 and 5. This is to prevent abuse.

Example: `-setmaxtickets 2`

### Set Moderation Command
``` 
-setmoderation <true/false>
```
With this command you can determine whether or not the Tickety moderation features should be enabled. This is useful when you have a dedicated bot for moderation, or if you don't want your support team to have moderation access.

Example: `-setmoderation false`

### Set Message Command
```
-setmsg
```
With this command you can set the message the will be sent in a ticket when a ticket is created.

Example:
```
User: -setmsg

Tickety: You can now set your welcome message, please send it in one message in this channel.
         You can use :user: to get it replaced with a mention.
         You can use }} to end the embed and send a message outside of the embed, this can be useful for a mention.
         Type -setmsg again to cancel.
         
User:    Welcome :user:,
         
         Please describe your issue carefully, and we will be right with you.
         
         With kind regards,
         Tickety Support}}:user:
        
Tickety: The message has been set.
```

### Set Prefix Command
```
-setprefix <prefix>
```
With this command you can set the command prefix for all of Tickety's commands.

::: tip
If you don't know what Tickety's prefix is at the moment in a certain server, just mention him (@Tickety). He will tell you what the prefix is.
:::

Example: `-setprefix !`

### Set Role Command
```
-setrole <@role>
```
With this command you can set the role that Tickety will treat as the admin role.

Example: `-setrole @Ticket Handlers`

### Redeem Premium Command
```
-redeem
```
With this command you can redeem a premium token on a server. Find out more about premium and how to get a premium token [here](/premium/).