## Objetivo

There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
- Usuario: **bandit31

## Solución

```
bandit31@bandit:/tmp/nuevo31$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit31@bandit:/tmp/nuevo31$ ls
repo
bandit31@bandit:/tmp/nuevo31$ cd rep
-bash: cd: rep: No such file or directory
bandit31@bandit:/tmp/nuevo31$ cd rep0
-bash: cd: rep0: No such file or directory
bandit31@bandit:/tmp/nuevo31$ cd repo
bandit31@bandit:/tmp/nuevo31/repo$ ls -la
total 20
drwxrwxr-x 3 bandit31 bandit31 4096 Feb 27 04:50 .
drwxrwxr-x 3 bandit31 bandit31 4096 Feb 27 04:50 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Feb 27 04:50 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Feb 27 04:50 .gitignore
-rw-rw-r-- 1 bandit31 bandit31  147 Feb 27 04:50 README.md
bandit31@bandit:/tmp/nuevo31/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/nuevo31/repo$ nano key.txt
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit31@bandit:/tmp/nuevo31/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/nuevo31/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/nuevo31/repo$ ls -a
.  ..  .git  .gitignore  key.txt  README.md
bandit31@bandit:/tmp/nuevo31/repo$ cat .gitignore
*.txt
bandit31@bandit:/tmp/nuevo31/repo$ rm .gitignore
bandit31@bandit:/tmp/nuevo31/repo$ git add key.txt
bandit31@bandit:/tmp/nuevo31/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   key.txt

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore

bandit31@bandit:/tmp/nuevo31/repo$ git commit -m "hi"
[master f559976] hi
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/nuevo31/repo$ git log
commit f559976d29a233674f98b93d074a722044759c0c (HEAD -> master)
Author: bandit31 <bandit31@overthewire.org>
Date:   Tue Feb 27 04:55:11 2024 +0000

    hi

commit 12c8b5c836110b00471d51a3d59bfb5efc1d8020 (origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:47 2023 +0000

    initial commit
bandit31@bandit:/tmp/nuevo31/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/nuevo31/repo$
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