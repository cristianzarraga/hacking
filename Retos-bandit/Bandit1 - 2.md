## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
- Usuario: **bandit1**

## Solución

```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ ls -la
total 24
-rw-r-----  1 bandit2 bandit1   33 Oct  5 06:19 -
drwxr-xr-x  2 root    root    4096 Oct  5 06:19 .
drwxr-xr-x 70 root    root    4096 Oct  5 06:20 ..
-rw-r--r--  1 root    root     220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root    3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root    root     807 Jan  6  2022 .profile
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas adicionales

### Lista de archivos en formato largo, incluidos los archivos ocultos

Escriba el comando `ls -l -a` o `ls -a -l` o `ls -la` o `ls -al` para listar archivos o directorios en un formato de tabla con información adicional, incluidos archivos o directorios ocultos:

Con **cat ./-** podemos abrir un archivo que tenga un "-" guion medio como nombre

## Referencias

[Dashed Filename - Learn How to Create/Remove/List/Read/Copy (webservertalk.com)](https://www.webservertalk.com/dashed-filename/)

[Special Characters (tldp.org)](https://tldp.org/LDP/abs/html/special-chars.html)

[El comando Linux LS: Cómo Listar archivos en un directorio + indicadores de opción (freecodecamp.org)](https://www.freecodecamp.org/espanol/news/el-comando-linux-ls-como-listar-archivos-en-un-directorio-indicadores-de-opcion/)