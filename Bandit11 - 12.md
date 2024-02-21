## Objetivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
- Usuario: **bandit11

## Solución

```bash
bandit11@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root     4096 Oct  5 06:20 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit12 bandit11   49 Oct  5 06:19 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit11@bandit:~$ wc data.txt
 1  4 49 data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```

## Notas adicionales

Se utiliza el comando tr para poder visualizar correctamente la informacion y encontrar la bandera, se le especifica que tome los caracteres de la a hasta la z en minusculas y mayusculas.

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[Base64 - Wikipedia](https://en.wikipedia.org/wiki/Base64)
[ROT13 - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/ROT13)