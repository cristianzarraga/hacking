## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución

Inspeccionamos con nano el programa en python y posteriormente observamos que evalua una entrada por el usuario, un numero de 4 digitos, al ingresarlo nos devuelve la bandera

```
czarragar-picoctf@webshell:~$ nano level1.py 
czarragar-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
czarragar-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias

