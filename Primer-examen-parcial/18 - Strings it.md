## Objetivo

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución

Ejecutamos el siguiente comando para convertir la salida a un archivo txt legible por humanos

strings strings > output.tx

```
czarragar-picoctf@webshell:~$ cat output.txt | grep pico
picoCTF{5tRIng5_1T_827aee91}
czarragar-picoctf@webshell:~$  

```

## Notas adicionales

strings
## Referencias
