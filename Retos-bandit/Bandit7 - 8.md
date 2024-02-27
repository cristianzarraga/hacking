## Objetivo

The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
- Usuario: **bandit7

## Solución

```bash
bandit7@bandit:~$ ls -la
total 4108
drwxr-xr-x  2 root    root       4096 Oct  5 06:19 .
drwxr-xr-x 70 root    root       4096 Oct  5 06:20 ..
-rw-r--r--  1 root    root        220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root       3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit8 bandit7 4184396 Oct  5 06:19 data.txt
-rw-r--r--  1 root    root        807 Jan  6  2022 .profile
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ cat data.txt | grep "millionth"
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```

## Notas adicionales

Utilizamos el wc data.txt para observar mas informacion sobre los rengolones. caracteres y palabras del archivo

usamos el pipe | grep "millionth" para localizar en especifico ese renglon donde se ubique dicha palabra que acabamos de especificar.

-n nos muestra en que linea se encuentra

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

