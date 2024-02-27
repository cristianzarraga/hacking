## Objetivo

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
- Usuario: **bandit20

## Solución

```
bandit20@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root      4096 Oct  5 06:20 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit21 bandit20 15600 Oct  5 06:19 suconnect
bandit20@bandit:~$ ./suconnect
Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
bandit20@bandit:~$ nc -lnvp 6678 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3064893
bandit20@bandit:~$ Listening on 0.0.0.0 6678

bandit20@bandit:~$ jobs
[1]+  Running                 nc -lnvp 6678 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
bandit20@bandit:~$
bandit20@bandit:~$ jobs
[1]+  Running                 nc -lnvp 6678 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
bandit20@bandit:~$ ^C
bandit20@bandit:~$
bandit20@bandit:~$ jobs
[1]+  Running                 nc -lnvp 6678 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
bandit20@bandit:~$
bandit20@bandit:~$ ./suconnect 6678
Connection received on 127.0.0.1 46260
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
bandit20@bandit:~$ NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

[1]+  Done                    nc -lnvp 6678 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$ jobs
bandit20@bandit:~$

```

## Notas adicionales


"SGID" redirects here. For the company which briefly used this stock ticker symbol, see [Silicon Graphics](https://en.wikipedia.org/wiki/Silicon_Graphics "Silicon Graphics").

The [Unix](https://en.wikipedia.org/wiki/Unix "Unix") and [Linux](https://en.wikipedia.org/wiki/Linux "Linux") access rights flags **setuid** and **setgid** (short for _set user identity_ and _set group identity_)[[1]](https://en.wikipedia.org/wiki/Setuid#cite_note-1) allow users to run an [executable](https://en.wikipedia.org/wiki/Executable "Executable") with the [file system permissions](https://en.wikipedia.org/wiki/File_system_permissions "File system permissions") of the executable's owner or group respectively and to change behaviour in directories. They are often used to allow users on a computer system to run programs with temporarily elevated privileges to perform a specific task. While the assumed user id or group id privileges provided are not always elevated, at a minimum they are specific.

The flags `setuid` and `setgid` are needed for tasks that require different privileges than what the user is normally granted, such as the ability to alter system files or databases to change their login password.[[2]](https://en.wikipedia.org/wiki/Setuid#cite_note-oreilly-2) Some of the tasks that require additional privileges may not immediately be obvious, though, such as the `[ping](https://en.wikipedia.org/wiki/Ping_(networking_utility) "Ping (networking utility)")` command, which must send and listen for [control packets](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol "Internet Control Message Protocol") on a network interface.

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)