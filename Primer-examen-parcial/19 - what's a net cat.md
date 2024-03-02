## Objetivo

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución

Era necesario ejecutar el comando NC para poder conectarnos a dicho dominio mediante el puerto especificado en las instrucciones

```
czarragar-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 64287
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_284be8f7}
 

```

## Notas adicionales

Consultamos la documentacion de NC 
## Referencias

[nc(1): arbitrary TCP/UDP connections/listens - Linux man page (die.net)](https://linux.die.net/man/1/nc)
