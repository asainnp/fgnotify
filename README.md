# fgnotify 
### Bash-Shell Script, Notifying Foreground Console (tty) with a message in up-right corner, (and restoring chars after period)
Asain Kujovic, march 2015.

Notes: 
- root(sudo) or tty-group permisions needed
- 3 external tools used:  >> od, dd, sed <<
- restore msg performed only when notify is still present
- color in sed hexa format x47 means 4(red)-bgc, 7(white)-fgc
