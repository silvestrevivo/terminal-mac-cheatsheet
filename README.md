# terminal-mac-cheatsheet
The terminal has two first things to learn: *The prompt* `$` is where you type the commands to execute, and the *root* `~` is just the **root user folder**. There are *three* types of commands:

+ Single: `$ date` => *$ command*

+ With extra: `$ echo "message"` => *$ command + extra*

+ With action and something extra: `$ cal 01 2018` => *$ command + (-option) + (something extra)*

Some examples of them:

```js
    $ whoami                => Prints out owner name of terminal
    $ date                  => do 19 apr 2018 21:34:12 CEST
    $ date -u               => vr 20 apr 2018 11:07:38 UTC
    $ cal                   => Current month
    $ cal 01 2018           => First month of 2018
    $ killall <application> => Closes application
    $ echo "message"        => Prints out 'message' on terminal
    $ echo "message        "=> Prints message in two lines
    $ echo "in two lines"
    $ echo $USER            => Prints out owner name of terminal
    $ echo $HOME            => Prints out root user directory
    $ say "message"         => The computer says the 'message' aloud
    $ man [command]         => Opens the manual for that command
    $ clear                 => Cleans the terminal
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
| writable/readable/editable| user name | group file | size | last modification | file name
---
## FILES MANAGEMENT
| Key/Command | Description |
| :-----------: | ----------- |
| touch [filename.extension] | Creates a new file |
| open [file] | Opens a file with its program by default |
| nano [file] | Opens a file with the nano editor of the terminal |
| nano -m [file] | Opens a file with nano editor and mouse as pointer |
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
| mkdir -p [dir]/[dir] | Creates nested directories |
| rmdir [dir] | Removes directory ( only operates on empty directories ) |
| [command] > [file] | Push output to file, keep in mind it will get overwritten |
| [command] >> [file] | Append output to existing file |
| [command] < [file] | Tell command to read content from a file |


## EDITION MANAGEMENT
| Key/Command | Description |
| :-----------: | ----------- |
| cat [file] | Prints out and concatenate files on screen terminal|
| cat - n [file] | Prints out and concatenate files with rule number next to |
| cat file01 > file02 | Overwrites the content from one file to another one |
| cat file01 >> file02 | Concatenates the content of both files on the second one |
| echo 'message' | Prints out 'message' on the screen terminal |
| echo "message" > [file] | Writes 'message' as content on file |
| echo "text" >> [file] | Adds 'message' as content at the end of file |
| more [file] | Prints out the file content targeting the beginning |
| less [file] | Output file content delivered in another space in th terminal |
| sort [file] | Sorts a file alphabetically |
| file [file] | Gives information about the file |
| file *.extension | Gives information about all files with that extension |
| pbcopy < [file] | Copies file contents to clipboard |
| pbpaste | Paste clipboard contents |
| pbpaste > [file] | Paste clipboard contents into file |


## PIPES
| Key/Command | Description |
| :-----------: | ----------- |
| [command1] \| [command2] | Uses the output of command1 to execute command2 |
| tail -n [file] | Shows the last n lines of the file |
| [command1] \| tail -n | Outputs the last n files of the command1 |
|  [command1] \| tail -n \| less | Outputs as less the last 3 lines of command1 |
| [command1] \| tail -n \| sort > [newfile] | Sort the last n files of command1 in a new file |


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
