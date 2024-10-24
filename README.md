# Screen-Command
The screen command in Linux is used to manage and switch between multiple terminal sessions. It allows users to create, detach, and reattach terminal sessions, which can be useful for a number of reasons:

`Long-running processes: Screen can ensure that long-running processes continue even if you log off or your connection drops.`

`Multitasking: Screen allows you to run multiple processes at once.`

`Unstable connections: Screen can help you maintain terminal sessions over unstable network connections.`

`Remote access: You can use screen to access multiple terminal sessions from a remote location.`

`Multiple users: Multiple remote computers can connect to the same screen session at once.`

# Install
| Linux distribution 				| Command to install Screen 				|
|---------------------------------------|---------------------------------------|
| Ubuntu or Debian | `sudo apt update && sudo apt install screen`		|
| Red Hat or CentOS	      | `yum install screen`				|
| RHEL derivatives like CentOS 8 or later	      | `sudo dnf update && sudo dnf install screen`				|

# Screen Quick Reference

## Basic

| Description 				| Command 				|
|---------------------------------------|---------------------------------------|
| Start a new session with session name | `screen -S <session_name>`		|
| List running sessions / screens	      | `screen -ls`				|
| Attach to a running session		        | `screen -x`				|
| Attach to a running session with name	| `screen -r <session_name>`		|
| Detach a running session		          | `screen -d <session_name>`		|
| Kill a running session                | `screen -X -S [session # you want to kill] kill` |
| Accessing a screen that is already attached | `screen -r -d [session name]` |

## Escape Key

All screen commands are prefixed by an escape key, by default Ctrl-a (that's Control-a, sometimes written ^a). To send a literal Ctrl-a to the programs in screen, use Ctrl-a a. This is useful when when working with screen within screen. For example Ctrl-a a n will move screen to a new window on the screen within screen. 

## Getting Out

| Description				| Command						|
|---------------------------------------|-------------------------------------------------------|
| detach 				| `Ctrl-a d`						|
| detach and logout (quick exit) 	| `Ctrl-a D D`						|
| exit screen 				| `Ctrl-a :` quit or exit all of the programs in screen.|
| force-exit screen 			| `Ctrl-a C-\` (not recommended) 			|

## Help

| Description	| Command			|
|---------------|-------------------------------|
| See help	| `Ctrl-a ?` (Lists keybindings)|

## Window Management

| Description				| Command								|
|---------------------------------------|-----------------------------------------------------------------------|
| Create new window 			| `Ctrl-a c`								|
| Change to last-visited active window 	| `Ctrl-a Ctrl-a` (commonly used to flip-flop between two windows)	|
| Change to window by number 		| `Ctrl-a <number>` (only for windows 0 to 9)				|
| Change to window by number or name 	| `Ctrl-a ' <number or title>`						|
| Change to next window in list 	| `Ctrl-a n` or `Ctrl-a <space>`					|
| Change to previous window in list 	| `Ctrl-a p` or `Ctrl-a <backspace>`					|
| See window list 			| `Ctrl-a "` (allows you to select a window to change to)		|
| Show window bar 			| `Ctrl-a w` (if you don't have window bar)				|
| Kill current window 			| `Ctrl-a k` (not recommended)						|
| Kill all windows 			| `Ctrl-a \` (not recommended)						|
| Rename current window 		| `Ctrl-a A`								|

## Split screen

| Description				| Command								|
|---------------------------------------|-----------------------------------------------------------------------|
| Split display horizontally 		| `Ctrl-a S`								|
| Split display vertically 		| `Ctrl-a |` or `Ctrl-a V` (for the vanilla vertical screen patch)	|
| Jump to next display region 		| `Ctrl-a tab`								|
| Remove current region 		| `Ctrl-a X`								|
| Remove all regions but the current one| `Ctrl-a Q`								|

## Misc

| Description						| Command								|
|-------------------------------------------------------|-----------------------------------------------------------------------|
| Redraw window 					| `Ctrl-a C-l`								|
| Enter copy mode 					| `Ctrl-a [` or `Ctrl-a <esc>` (also used for viewing scrollback buffer)|
| Paste 						| `Ctrl-a ]`								|
| Monitor window for activity 				| `Ctrl-a M`								|
| Monitor window for silence 				| `Ctrl-a _`								|
| Enter digraph (for producing non-ASCII characters) 	| `Ctrl-a Ctrl-v`							|
| Lock (password protect) display 			| `Ctrl-a x`								|
| Enter screen command 					| `Ctrl-a :`								|
| Enable logging in the screen session 			| `Ctrl-a H`								|

## Scrolling 

| Description | Command |
|-----|------|
| Enter scrolling mode | Ctrl-a esc |
| Scroll Up | Ctrl-u |
| Scroll Down | Ctrl-d |
| Exit scrolling mode | esc esc |

This section is a contribution from: [@mickpbarry](https://gist.github.com/mickpbarry) & [@jctosta](https://gist.github.com/jctosta)

