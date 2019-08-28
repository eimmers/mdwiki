#### execute local script on remote server via ssh ####
```
ssh <host> "bash -s" -- < ./script.sh
```

#### Exit if statement fails (conditinal expression)
```
test -b /dev/sdddd || { echo >&2 "Disk /dev/sddd does not exist...exit"; exit 1; }
```

#### show complete username with ps
```
alias psx='export PS_FORMAT="user:12,pid,%cpu,%mem,vsz,rss,tty,stat,start,time,command"; ps ax'
```

#### Ignore grep with 'ps grep'
```
ps aux | grep "[i]tsme"
```
By putting the brackets around the letter and quotes around the beginning of the string you search for the regex, which says, "Find the character 'i' followed by 'tsme'."

#### force dutch output (or any other language)
```
LC_ALL=nl_NL.utf8  date '+%d %B %Y %H:%m:%S'
```
locale -a (show all locales)
