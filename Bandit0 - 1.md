## Objetivo

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: **bandit0**
- Usuario: **bandit0**

## Solución

```bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$
```

## Notas adicionales

Aprendí a utilizar los comandos "ls" para listar los archivos del directorio.
Aprendí a utilizar el comando "cat" para abrir el archivo readme.

## Referencias