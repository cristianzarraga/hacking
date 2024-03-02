## Objetivo

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución

Era necesario editar la identacion para lograr correr el script correctamente

```
czarragar-picoctf@webshell:~$ nano fixme1.py 
czarragar-picoctf@webshell:~$ python3 fixme1.py 
  File "/home/czarragar-picoctf/fixme1.py", line 20
    print(flag)
IndentationError: unexpected indent
czarragar-picoctf@webshell:~$ nano fixme1.py 
czarragar-picoctf@webshell:~$ python3 fixme1.py 
picoCTF{1nd3nt1ty_cr1515_6a476c8f}
czarragar-picoctf@webshell:~$ ^C

```

## Notas adicionales

Es necesario tomar en cuenta la identacion en el script
## Referencias
