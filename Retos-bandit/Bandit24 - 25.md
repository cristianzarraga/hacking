## Objetivo

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
- Usuario: **bandit24

## Solución

Para poder acceder a la bandera se genero un script que siguiera las reglas que se piden para poder acceder a la contraseña y se ejecutara en un ciclo for hasta poder conseguir el resultado, por lo cual el script fue el siguiente:

```
#!/bin/bash

bandit24Pass=VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

for pin in {0000..9999}; do
        echo "$bandit24Pass $pin"
done | nc localhost 30002
```

```
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
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