## Objetivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
- Usuario: **bandit9

## Solución

```bash
bandit9@bandit:~$ ls -la
total 40
drwxr-xr-x  2 root     root     4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root     4096 Oct  5 06:20 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit10 bandit9 19379 Oct  5 06:19 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit9@bandit:~$ wc data.txt
   67   424 19379 data.txt
bandit9@bandit:~$ strings data.txt | grep ==
x]T========== theG)"
========== passwordk^
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```

## Notas adicionales

Con strings buscamos cadenas dentro del archivo de texto y asi mismo con el comando grep establecemos las reglas de que debe ser precedido por el signo de "="

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

