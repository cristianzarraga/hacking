## Objetivo

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
- Usuario: **bandit4

## Solución

```bash
bandit4@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Oct  5 06:19 .
drwxr-xr-x 70 root root 4096 Oct  5 06:20 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
drwxr-xr-x  2 root root 4096 Oct  5 06:19 inhere
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit4@bandit:~$ ls -la inhere
total 48
drwxr-xr-x 2 root    root    4096 Oct  5 06:19 .
drwxr-xr-x 3 root    root    4096 Oct  5 06:19 ..
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file00
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file01
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file02
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file03
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file04
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file05
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file06
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file07
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file08
-rw-r----- 1 bandit5 bandit4   33 Oct  5 06:19 -file09
bandit4@bandit:~$ file inhere/*
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data
bandit4@bandit:~$
bandit4@bandit:~$ cat inhere/-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~$
```

## Notas adicionales

En esta ejercicio lo que vamos a utilizar es el comando FILE con el argumento de * para identificar el tipo de archivo y descubrir cual archivo es el que es humanamente leible. 

encontramos un archivo con texto ASCII

Con file inhere/*

Vemos los archivos y el tipo de datos que contiene
## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)

