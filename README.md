# fgnotify 
### Bash-Shell Script, Notifying Foreground Console (tty) with a message in up-right corner, (and restoring chars after period)
Asain Kujovic, march 2015.

Notes: 
- root(sudo) or tty-group permisions needed
- 3 external tools used:  >> od, dd, sed <<
- restore msg performed only when notify is still present
- color in sed hexa format x47 means 4(red)-bgc, 7(white)-fgc

Install:
> git clone https://github.com/asainnp/fgnotify.git
> cd fgnotify
> cp fgnotify /usr/bin/.

Example usage:
> sudo fgnotify "new mail in inbox"
Running it on tty / some X remote terminal / crone / detached process / remote SSH, ... message should be displayed on active-foreground tty console of computer running this process.
