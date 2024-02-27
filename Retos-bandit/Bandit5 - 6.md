## Objetivo

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
- Usuario: **bandit5

## Solución

```bash
bandit5@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root    4096 Oct  5 06:19 .
drwxr-xr-x 70 root root    4096 Oct  5 06:20 ..
-rw-r--r--  1 root root     220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root    3771 Jan  6  2022 .bashrc
drwxr-x--- 22 root bandit5 4096 Oct  5 06:19 inhere
-rw-r--r--  1 root root     807 Jan  6  2022 .profile
bandit5@bandit:~$ find inhere -readable -type f -size 1033c
inhere/maybehere07/.file2
bandit5@bandit:~$ cat inhere/maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Notas adicionales

.-readable

Nos servira este comando para identificar los archivos que pueden ser leidos

-type f

Para filtrar los archivos que solo sean archivos y no directorios

-size 1033

Para identificar el archivo que tenga ese peso en bytes

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

