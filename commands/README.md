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
| -status |  Get information about the status of Tickety | [click](#status-command) |

## User Ticket Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -new | Create a new ticket | [click](#new-ticket-command) |
| -close | Close the ticket you're currently in | [click](#close-ticket-command) |
| -info | Get the info of a ticket | [click](#info-command) |
| -transcript| Get a transcript of the conversation | [click](#transcript-command) |

## Admin Ticket Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -rename | Rename a ticket | [click](#rename-ticket-command) |
| -add | Add a user to a ticket | [click](#add-to-ticket-command) |
| -closeall | Close **ALL** open tickets| [click](#close-all-tickets-command) |

## Moderation Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -blacklist | Block this user from performing Tickety commands | [click](#blacklist-command) |
| -unblacklist | Allow this user to perform Tickety commands again. | [click](#unblacklist-command) |
| -blacklists | View all blacklists for this server | [click](#blacklists-command) |

## Configuration Commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -setup | Setup the admin role for Tickety | [click](#setup-command) |
| -setlang | Set the language | [click](#set-language-command) |
| -setcategory | Set the category tickets will be created in | [click](#set-category-command) |
| -setmsg | Set the welcome message for new tickets | [click](#set-message-command) |
| -setname | Set the name tickets will be created with | [click](#set-name-command) |
| -setlog | Set the logging channel | [click](#set-log-command) |
| -setrole | Set the admin role | [click](#set-role-command) |
| -settranscriptlog | Set the log all transcripts will be sent in | [click](#set-transcript-log-command) |
| -setprefix | Set the command prefix | [click](#set-prefix-command) |
| -setopen | Determine if you want users to be able to open tickets | [click](#set-open-command) |
| -setmaxtickets | Set the amount of tickets one user can have | [click](#set-max-tickets-command) |

## Premium commands
| Command | Description | Guide |
| ------- | ----------- | ----- |
| -credits | View all of your premium credits| [click](#premium-credits-command) |
| -redeem | Redeem a premium token on this server | [click](#redeem-premium-command) |
| -removepremium | Remove premium in this server, to use it in another server| [click](#remove-premium-command) |

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

### Status command
```
-status
```
The status command will show Tickety's current status and other information

### New Ticket Command
```
-new [@user] [subject]
```
This command creates a new ticket for the executing user. Admins can tag a user as the first argument to open a ticket under their name.
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

### Info Command
```
-info
```
This command can only be executed inside a ticket channel. It will give basic information about a ticket.
It will return the creator of the ticket, the date of creation, the ticket id and the subject of the ticket.

### Transcript Command
```
-transcript [html/txt]
```
This command can only be executed inside a ticket channel. It will send a transcript of the full conversation.
You can either give `html` or `txt` as argument, which respectively return a html version or a text version of the transcript.
When no argument is provided a html document will be returned.

Example: `-transcript txt`

### Rename Ticket Command
```
-rename <name>
```
This command can only be executed inside a ticket channel. It will rename the ticket to the given name.

Example: `-rename report`, will rename a ticket called `ticket-0001` to `report-0001`.

### Add To Ticket Command
```
-add <@user> [#channel]
```
This command can add users to a ticket channel. 
When executed in a ticket channel you will have to provide the user ID as the first argument.
When executed outside a ticket channel you can mention the user as first argument, and mention the channel as the second argument.
 
Example inside ticket: `-add 352854019934257156`
Example outside of ticket: `-add @Stan#8888 #ticket-0001`

### Close all tickets command
```
-closeall
```
This command will close **all** tickets in your esrver.
When executed, you are asked a confirmation similar to when closing a ticket. This command can be dangerous, as tickets can not be reopened after they're closed.
::: danger
Use this command carefully!
:::


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

### Setup command
```
-setup
```
This command can be used once to set up the `Support Team` role automatically, and has no use after the role is made.

### Set language command
```
-setlang <language code>
```
Set the language for tickety.  

Example: `-setlang nl` will change the bot to Dutch in your server.

### Set category command
```
-setcategory <name>
```
With this command you can set the category that tickets will be created in.

Example: `-setcategory tickets`

### Set message command
```
-setmsg <message>
```
Sets the message that is send when a new ticket is opened. You can use the placeholder :user: to tag the user.

Example: `-setmsg Hello, thank you for opening a ticket :user:!`

### Set name command
```
-setname <name>
```
With this command, you can change the base name for tickets. By default, when a new ticket is made the channel will be named `ticket-####`.  
With the `-setname` command, you can change this to any base name you wish.

Example `-setname order`, when a new ticket is openend it will be named `order-####`

### Set log command
```
-setlog [#channel/disable]
```
With this command you can set the channel in which the ticket log messages will be sent. To disable the ticket log just put `disable` as the channel

Example to set a channel: `-setlog #tickets-log`
Example to disable log: `-setlog disable`

### Set role command
```
-setrole <@role>
```
With this command you can set the role that Tickety will treat as the admin role.  
This allows you to change the default `Support Team` role to a different role.  

Example: `-setrole @Ticket Handlers`

### Set transcript log command
```
-settranscriptslog [#channel/disable[
```
With this command you can set the channel in which all the transcripts will be sent. To disable the transcript log just put `disable` as the channel

::: warning
You generally want this channel to not be public to all users, because all transcripts will be sent here.
:::

Example to set a channel: `-settranscriptslog #transcripts-log`
Example to disable log: `-settranscriptslog disable`

### Set prefix Command
```
-setprefix <prefix>
```
With this command you can set the command prefix for all of Tickety's commands.

::: tip
If you don't know what Tickety's prefix is at the moment in a certain server, just mention him (@Tickety). He will tell you what the prefix is.
:::

Example: `-setprefix !`

### Set open command
```
-setopen <true/false>
```
With this command you can determine whether or not users should be able to open tickets. This is useful for when you're being raided, or when your support team is inactive/offline.

Example: `-setopen true`

### Set max tickets command
``` 
-setmaxtickets <amount>
```
Set the maximum amount of tickets that one user can have in your server. Has to range between 1 and 5. This is to prevent abuse.

Example: `-setmaxtickets 2`

### Premium credits command
```
-credits
```
View all your premium credits, and wether or not they are available. More detailed information is available [here](https://panel.tickety.net/premium)

### Redeem Premium Command
```
-redeem
```
With this command you can redeem a premium token on a server. Find out more about premium and how to get a premium token [here](/premium/).

### Remove premium command
```
-removepremium
```
With this command you can remove premium from a server to make the credit available again.