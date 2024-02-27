## Objetivo

There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
- Usuario: **bandit27

## Solución

```
bandit27@bandit:/tmp/nuevo27$ git clone "ssh://bandit27-git@localhost:2220/home/bandit27-git/repo"
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/nuevo27$ ls
repo
bandit27@bandit:/tmp/nuevo27$ ls -a
.  ..  repo
bandit27@bandit:/tmp/nuevo27$ cd repo
bandit27@bandit:/tmp/nuevo27/repo$ ls -la
total 16
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 27 04:17 .
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 27 04:17 ..
drwxrwxr-x 8 bandit27 bandit27 4096 Feb 27 04:17 .git
-rw-rw-r-- 1 bandit27 bandit27   68 Feb 27 04:17 README
bandit27@bandit:/tmp/nuevo27/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/nuevo27/repo$
```


## Notas adicionales

Se debe utilizar el comando git clone para copiar el repositorio y no olvidar poner enseguida de localhost el puerto 2220


## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
[cron (Unix) - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cron_(Unix))