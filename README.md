# bashpromptcolours
Notes on how to setup prompt colouring for bash. Great for when you have multiple hosts that are all similar.

Credit goes to https://phoenixnap.com/kb/change-bash-prompt-linux. I built the below knowledge and string from that page.

## Command
Below to setup the bash prompt. Replace WORDS string with your own message.
```
echo "PS1='\[\e[1;31m\]WORDS \[\e[2;35m\]\u@\h\[\e[0;32m\][\w]\\$ \[\e[0m\]'" >> /etc/profile
```

### Colours list
These colour codes are followed by an `m` 
* 30 – Black
* 31 – Red
* 32 – Green
* 33 – Brown
* 34 – Blue
* 35 – Purple
* 36 – Cyan
* 37 – Light gray

### Typeface list
These codes prepend the colour codes 
* 0 – Normal
* 1 – Bold (bright)
* 2 – Dim
* 4 – Underlined

### Options list
These codes are used to perform specific funtions such as listing the hostname and username
*    \a – A bell character
*    \d – Date (day/month/date)
*    \D{format} – Use this to call the system to respond with the current time
*    \e – Escape character
*    \h – Hostname (short)
*    \H – Full hostname (domain name)
*    \j – Number of jobs being managed by the shell
*    \l – The basename of the shells terminal device
*    \n – New line
*    \r – Carriage return
*    \s – The name of the shell
*    \t – Time (hour:minute:second)
*    \@ – Time, 12-hour AM/PM
*    \A – Time, 24-hour, without seconds
*    \u – Current username
*    \v – BASH version
*    \V – Extra information about the BASH version
*    \w – Current working directory ($HOME is represented by ~)
*    \W – The basename of the working directory ($HOME is represented by ~)
*    \! – Lists this command’s number in the history
*    \# – This command’s command number
*    \$ – Specifies whether the user is root (#) or otherwise ($)
*    \\– Backslash
*    \[ – Start a sequence of non-displayed characters (useful if you want to add a command or instruction set to the prompt)
*    \] – Close or end a sequence of non-displayed characters
