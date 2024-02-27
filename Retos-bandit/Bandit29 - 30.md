## Objetivo

There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
- Usuario: **bandit29

## Solución

```
bandit29@bandit:/tmp/nuevo29$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/nuevo29$ ls
repo
bandit29@bandit:/tmp/nuevo29$ cd repo
bandit29@bandit:/tmp/nuevo29/repo$ ls -la
total 16
drwxrwxr-x 3 bandit29 bandit29 4096 Feb 27 04:37 .
drwxrwxr-x 3 bandit29 bandit29 4096 Feb 27 04:36 ..
drwxrwxr-x 8 bandit29 bandit29 4096 Feb 27 04:37 .git
-rw-rw-r-- 1 bandit29 bandit29  131 Feb 27 04:37 README.md
bandit29@bandit:/tmp/nuevo29/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/nuevo29/repo$ git log
commit 4364630b3b27c92aff7b36de7bb6ed2d30b60f88 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    fix username

commit fca34ddb7d1ff1f78df36538252aea650b0b040d
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/nuevo29/repo$ git checkout fca3
Note: switching to 'fca3'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at fca34dd initial commit of README.md
bandit29@bandit:/tmp/nuevo29/repo$ git branch
* (HEAD detached at fca34dd)
  master
bandit29@bandit:/tmp/nuevo29/repo$ git checkout master
Previous HEAD position was fca34dd initial commit of README.md
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
bandit29@bandit:/tmp/nuevo29/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
bandit29@bandit:/tmp/nuevo29/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/nuevo29/repo$ git checkout mdev
error: pathspec 'mdev' did not match any file(s) known to git
bandit29@bandit:/tmp/nuevo29/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/nuevo29/repo$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
bandit29@bandit:/tmp/nuevo29/repo$ git log
commit 1d160de5f8f647f00634bbf3d49b9244275217b6 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    add data needed for development

commit 73d0f769233ffc2f59595412e22f41afc6218c04
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    add gif2ascii

commit 4364630b3b27c92aff7b36de7bb6ed2d30b60f88 (origin/master, origin/HEAD, master)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    fix username

commit fca34ddb7d1ff1f78df36538252aea650b0b040d
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/nuevo29/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/nuevo29/repo$
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