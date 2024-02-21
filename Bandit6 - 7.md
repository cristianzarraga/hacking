## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
- Usuario: **bandit6

## Solución

```bash
bandit6@bandit:~$ ls /
bin   dev      etc         home     lib    lib64   lost+found  mnt  proc  run   snap  sys  usr
boot  drifter  formulaone  krypton  lib32  libx32  media       opt  root  sbin  srv   tmp  var
bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

## Notas adicionales

ls /
Lista la raiz del directorio en donde estamos posicionados.

Utilizamos el comando find / para buscar en la raiz
Agregamos el filtro -type f para buscar solo archivos
Filtro -user bandit7 para buscar en ese usuario en especifico
Filtro -size 33c para localizar ese tipo de tamaño de archivo

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

