# terminal-mac-cheatsheet
The terminal has two first things to learn: *The prompt* `$` is where you type the commands to execute, and the *root* `~` is just the **root user folder**. There are *three* types of commands:

+ Single: `$ date` => *$ command*

+ With extra: `$ echo "message"` => *$ command + extra*

+ With action and something extra: `$ cal 01 2018` => *$ command + (-option) + (something extra)*

Some examples of them:

```js
    $ whoami                => Print out owner name of terminal
    $ date                  => do 19 apr 2018 21:34:12 CEST
    $ date -u               => vr 20 apr 2018 11:07:38 UTC
    $ cal                   => Current month
    $ cal 01 2018           => First month of 2018
    $ killall <application> => Close application
    $ echo "message"        => Print out 'message' on terminal
    $ echo "message        "=> Print message in two lines
    $ echo "in two lines"
    $ echo $USER            => Print out owner name of terminal
    $ echo $HOME            => Print out root user directory
    $ say "message"         => The computer says the 'message' aloud
    $ clear                 => Clean the terminal
    $ reset                 => Resets de terminal display
    $ top                   => Displays active processes: `q` to quit
    $ exit                  => End of terminal session

```
---


## SHORTCUTS

| Key/Command | Description |
| :---------: | ----------- |
| Tab | Auto-complete files and folders names|
| Ctrl + A| Go to the beginning of the line where you are currently working on|
| Ctrl + E| Go to the end of the line where you are currently working on |
| Ctrl + Q, Ctrl + U | Clears the current line |
| Ctrl + W, Cmnd + Shift + ← | Cut one word backwardd using white space as delimiter |
| Ctrl + K | Clears the line after cursor |
| Ctrl + L | Clean the terminal no deleting content |
| Cmnd + K | Clean de terminal deleting content |
| Ctrl + C | Kill whatever you are runing |
| Alt + → | Move cursor one word forward |
| Alt + ← | Move cursor one word backward |
| Ctrl + D | Exit the current shell |


## NAVIGATION
| Key/Command | Description |
| :---------: | ----------- |
| . | current directory |
| .. | Parent directory |
| cd .. | Move one level up |
| cd ../.. | Move two levels up |
| cd, cd ~ | Move to user directory |
| cd / | Move to root of drive directory |
| cd [folder] | Get into directory |
| cd - | Go to previous directory |
| pwd | Get current path directory |
| open . | Open current directory on Finder |


## LIST
| Key/Command | Description |
| :---------: | ----------- |
| ls | Short listing |
| ls -l | Long listing |
| ls -a | Listing including hidden files |
| ls -t | Listing by update |
| ls -lh | Long listing with Human readable file sizes |
| ls -F | Listing folders and executable files |
| ls -S | Listing files sorted by size |
| ls -althFS | Combining all previous options |
| ls [folder] | Listing a folder one level up |
---
When we type `ls -l` the result has the next pattern:
```
    drwxr-xr-x 5  cc  eng  4096 Jun 24 16:51  action
    drwxr-xr-x 4  cc  eng  4096 Jun 24 16:51  comedy
    drwxr-xr-x 6  cc  eng  4096 Jun 24 16:51  drama
    -rw-r--r-- 1  cc  eng     0 Jun 24 16:51  genres.txt
```
Each column means:

| drwxr-xr-x 5 | cc | eng | 4096 | Jun 24 16:51 | action |
| :----------: |:-: | :-: | :--: | :----------: | :----: |
| write/read/edit| user name | group file | size | last modification | file name
---
## FILES MANAGEMENT
| Key/Command | Description |
| :-----------: | ----------- |
| touch [filename.extension] | Creates a new file |
| open [file] | Opens a file with its program by default |
| nano [file] | Opens a file with the nano editor of the terminal |
| pico [file] | Opens a file with the nano editor of the terminal |
| vim [file] | Opens file with Vim editor |
| :q | Exit from Vim editor without save |
| :qw | Exit from Vim editor saving changes |
| rm [filename] | Deteles single file |
| rm -i [file]  | Deletes a file with confirmation |
| rm -f [file]  | Deletes a file without confirmation |
| rm -rf [dir], rm -R [dir]  | Removes a directory and its content |
| rm [folder]/* | Deltes all files in  a |
| cp [file] [newfile] | Copy file to file |
| cp [file] [dir] | Copies file to directory |
| cp -rv source/. dest/ | Copies all content from folder to folder |
| mv [file] [dir] | Moves file to directory |
| mv [file] [new filename] | Renames file in same directory |
| *.[extention] | Selects all files with that extension |
| * . * | Selects all the files |
| leters*.* | Selects all files which begins with [leters]|


## DIRECTORIES MANAGEMENT
| Key/Command | Description |
| :-----------: | ----------- |
| mkdir [dir] | Creates new directory |
| mkdir [dir] && cd [dir] | Creates and enter in new directory |
| mkdir -p [dir]/[dir] | Create nested directories |
| rmdir [dir] | Remove directory ( only operates on empty directories ) |


## EDITION MANAGEMENT
| Key/Command | Description |
| :-----------: | ----------- |
| cat [file] | Print out and concatenate files on screen terminal|
| cat - n [file] | Print out and concatenate files with rule number next to |


## HISTORY
| Key/Command | Description |
| :-----------: | ----------- |
| history | Shows complete command history |
| history n | Shows the last n commands of historial |
| ctrl-r | Interactively search through previously typed commands |
| ![value] | Execute the last command typed that starts with ‘value' |
| ![value]:p | Print to the console the last command typed that starts with ‘value’ |
| !! | Execute the last command typed |
| !!:p | Print to the console the last command typed |


## CHAINING COMMANDS
| Key/Command | Description |
| :-----------: | ----------- |
| [command-a]; [command-b] | Run command A and then B, regardless of success of A|
| [command-a] && [command-b] | Run command B if A succeeded |
| [command-a] || [command-b] | Run command B if A failed |
| [command-a] & | Run command A in background |


## HELP
| Key/Command | Description |
| :-----------: | ----------- |
| [command] -h , [command] --help | Offers help |
| man [command] | Show the help manual for [command] |
| whatis [command] | Gives a one-line description of [command] |
| apropos [search-pattern] | Searches for command with keywords in description |


---

## MISCELANEA

```js
    $ man [command]     => manual
    $ nano              => open
    $ sudo              => owner
````
---
