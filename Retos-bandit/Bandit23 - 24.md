## Objetivo

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
- Usuario: **bandit23

## Solución

```
bandit23@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Oct  5 06:19 .
drwxr-xr-x 70 root root 4096 Oct  5 06:20 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit23@bandit:~$ cd /etc/cron.d/
bandit23@bandit:/etc/cron.d$ ls -la
total 56
drwxr-xr-x   2 root root  4096 Oct  5 06:20 .
drwxr-xr-x 106 root root 12288 Oct  5 06:20 ..
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Oct  5 06:19 cronjob_bandit22
-rw-r--r--   1 root root   122 Oct  5 06:19 cronjob_bandit23
-rw-r--r--   1 root root   120 Oct  5 06:19 cronjob_bandit24
-rw-r--r--   1 root root    62 Oct  5 06:19 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Oct  5 06:20 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/etc/cron.d$ which bash
/usr/bin/bash
bandit23@bandit:/etc/cron.d$ cat /var/spool/bandit24/foo
cat: /var/spool/bandit24/foo: Permission denied
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit23@bandit:/etc/cron.d$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ ls
ls: cannot open directory '.': Permission denied
bandit23@bandit:/var/spool/bandit24/foo$
bandit23@bandit:/var/spool/bandit24/foo$
bandit23@bandit:/var/spool/bandit24/foo$ mkdir /tmp/pass_2024
bandit23@bandit:/var/spool/bandit24/foo$ cd /tmp/pass_2024
bandit23@bandit:/tmp/pass_2024$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/pass_2024$ ls
script.sh
bandit23@bandit:/tmp/pass_2024$ ls -l
total 4
-rw-rw-r-- 1 bandit23 bandit23 69 Feb 26 23:27 script.sh
bandit23@bandit:/tmp/pass_2024$ cat script.sh
#!/bin/bash
cat  /etc/bandit_pass/bandit24 > /tmp/pass_2024/password
bandit23@bandit:/tmp/pass_2024$
bandit23@bandit:/tmp/pass_2024$
bandit23@bandit:/tmp/pass_2024$ touch password
bandit23@bandit:/tmp/pass_2024$ ls
password  script.sh
bandit23@bandit:/tmp/pass_2024$ ls -l
total 4
-rw-rw-r-- 1 bandit23 bandit23  0 Feb 26 23:28 password
-rw-rw-r-- 1 bandit23 bandit23 69 Feb 26 23:27 script.sh
bandit23@bandit:/tmp/pass_2024$ chmod 777 -R /tmp/pass_2024
bandit23@bandit:/tmp/pass_2024$ ls -l
total 4
-rwxrwxrwx 1 bandit23 bandit23  0 Feb 26 23:28 password
-rwxrwxrwx 1 bandit23 bandit23 69 Feb 26 23:27 script.sh
bandit23@bandit:/tmp/pass_2024$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
bandit23@bandit:/tmp/pass_2024$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/pass_2024$
```

## Notas adicionales

A _crontab_ file contains instructions to the **[cron](https://linux.die.net/man/8/cron)**(8) daemon of the general form: "run this command at this time on this date". Each user has their own crontab, and commands in any given crontab will be executed as the user who owns the crontab. Uucp and News will usually have their own crontabs, eliminating the need for explicitly running **[su](https://linux.die.net/man/1/su)**(1) as part of a cron command.

Blank lines and leading spaces and tabs are ignored. Lines whose first non-space character is a pound-sign (#) are comments, and are ignored. Note that comments are not allowed on the same line as cron commands, since they will be taken to be part of the command. Similarly, comments are not allowed on the same line as environment variable settings.

An active line in a crontab will be either an environment setting or a cron command. An environment setting is of the form,

name = value

where the spaces around the equal-sign (=) are optional, and any subsequent non-leading spaces in _value_ will be part of the value assigned to _name_. The _value_ string may be placed in quotes (single or double, but matching) to preserve leading or trailing blanks.

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
[cron (Unix) - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cron_(Unix))