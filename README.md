# fgnotify 
#### Bash-Shell Script, Notifying Foreground Console (active TTY) 
*notifying by:* show message in upper-right corner, and restore underlying chars after period.

Asain Kujovic, march 2015.

Notes: 
- root(sudo) or tty-group permisions needed
- 3 external tools used:  >> od, dd, sed <<
- restore msg performed only when notify is still present
- color in sed hexa format x47 means 4(red)-bgc, 7(white)-fgc
- 16 lines of active code

Install:
> git clone https://github.com/asainnp/fgnotify.git  
> cd fgnotify  
> sudo cp fgnotify /usr/bin/.  

Example run:
> sudo fgnotify "new mail in inbox"

Running it inside tty /some X remote terminal /crone /detached process /remote SSH /inputrc-keyBind ...  
should display message on active-foreground tty console of computer running this process,  
over underlaying shell-prompt/screen/tmux/login-prompt... that runs inside the fg-tty.
