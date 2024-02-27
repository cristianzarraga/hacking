## Objetivo

Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
- Usuario: **bandit26

## Solución

Se ingresa al igual que en el ejercicio anterior, disminuyendo el tamaño de la pantalla para que aparezca la funcionalidad MORE, en donde introducimos el siguiente comando para crear un bash dentro de bandit 26

:shell=/bin/bash
:shell

Asi mismo ya estariamos dentro de bandit26

```
bandit26@bandit:~$ ls -la
total 44
drwxr-xr-x  3 root     root      4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root      4096 Oct  5 06:20 ..
-rwsr-x---  1 bandit27 bandit26 14876 Oct  5 06:19 bandit27-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root      4096 Oct  5 06:19 .ssh
-rw-r-----  1 bandit26 bandit26   258 Oct  5 06:19 text.txt
bandit26@bandit:~$ ./bandit27-do
Run a command as another user.
  Example: ./bandit27-do id
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```


## Notas adicionales



## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
[cron (Unix) - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cron_(Unix))