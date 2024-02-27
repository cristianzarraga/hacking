## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
- Usuario: **bandit8

## Solución

```bash
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Oct  5 06:19 .
drwxr-xr-x 70 root    root     4096 Oct  5 06:20 ..
-rw-r--r--  1 root    root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Oct  5 06:19 data.txt
-rw-r--r--  1 root    root      807 Jan  6  2022 .profile
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```

## Notas adicionales

Sort :  Comando que nos ayuda a ordenar las líneas en un archivo de texto

uniqu -u: Comando que identifica las líneas en un archivo de texto que no se repiten

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

