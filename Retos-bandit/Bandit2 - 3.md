## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
- Usuario: **bandit2**

## Solución

```bash
bandit2@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root    root    4096 Oct  5 06:19 .
drwxr-xr-x 70 root    root    4096 Oct  5 06:20 ..
-rw-r--r--  1 root    root     220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root    3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root    root     807 Jan  6  2022 .profile
-rw-r-----  1 bandit3 bandit2   33 Oct  5 06:19 spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```

## Notas adicionales

Para abrir un archivo con espacios debemos introducir el comando CAT acompañado de comillas

**CAT "SPACES IN THIS FILENAME"**

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)

