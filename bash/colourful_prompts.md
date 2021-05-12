1.2.1 Open terminal. <br />
1.2.2 Use your favourite text editor to edit the .bashrc file (e.g. nano): `nano ~/.bashrc`. <br />
1.2.3 Enter the piece of code under:<br />
```
# Custom parameters
tprompt () {
    local bold=$(tput bold)
    local red=$(tput setaf 1)
    local green=$(tput setaf 2)
    local magenta=$(tput setaf 5)
    local cyan=$(tput setaf 6)
    local plain=$(tput sgr0)
    printf -v PS1 '%s' \
		'\[\033[1;36m\]' \
		'\u\[\033[1;31m\]' \
		'@\[\033[1;32m\]' \
		'\h:\[\033[1;35m\]' \
		'\w\[\033[1;31m\]' \
		'\$\[\033[0m\] '
}
tprompt

tput () {
    printf '\\['
    command tput "$@"
    printf '\\]'
}
``` 
1.2.4 Enter `source ~/.bashrc` <br />
1.2.5 Restart terminal.
