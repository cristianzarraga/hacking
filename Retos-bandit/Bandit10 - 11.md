## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
- Usuario: **bandit10

## Solución

```bash
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Oct  5 06:19 .
drwxr-xr-x 70 root     root     4096 Oct  5 06:20 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Oct  5 06:19 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit10@bandit:~$ wc data.txt
 1  1 69 data.txt
 bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

## Notas adicionales

Se utiliza base64 -d para convertir los caracteres en dicha base y poder observar correctamente la informacion y encontrar la bandera

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[Base64 - Wikipedia](https://en.wikipedia.org/wiki/Base64)