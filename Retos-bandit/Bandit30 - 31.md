## Objetivo

There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
- Usuario: **bandit30

## Solución

```
bandit30@bandit:/tmp/nuevo30$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit30@bandit:/tmp/nuevo30$ ls
repo
bandit30@bandit:/tmp/nuevo30$ cd repo
bandit30@bandit:/tmp/nuevo30/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Feb 27 04:45 .
drwxrwxr-x 3 bandit30 bandit30 4096 Feb 27 04:45 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Feb 27 04:45 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Feb 27 04:45 README.md
bandit30@bandit:/tmp/nuevo30/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/nuevo30/repo$ git log
commit d39631d73f786269b895ae9a7b14760cbf40a99f (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:45 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/nuevo30/repo$ git branch
* master
bandit30@bandit:/tmp/nuevo30/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/nuevo30/repo$ git tag
secret
bandit30@bandit:/tmp/nuevo30/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/nuevo30/repo$
```


## Notas adicionales

Se debe utilizar el comando git clone para copiar el repositorio y no olvidar poner enseguida de localhost el puerto 2220

Git log - para visualizar los commits
Git show - visualizamos el contenido introduciendo el respectivo hash
git log
git checkout dev
git status



## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
[cron (Unix) - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cron_(Unix))