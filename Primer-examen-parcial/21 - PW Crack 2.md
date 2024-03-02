## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución

Exploramos el codigo y convertimos en cyberchef desde numeros hexadecimales a decimales para cumplir el IF y asi obtener la bandera


```
czarragar-picoctf@webshell:~$ nano level2.py 
czarragar-picoctf@webshell:~$ python3 level2.py 
Please enter correct password for flag: 4ce9
That password is incorrect
czarragar-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
czarragar-picoctf@webshell:~$ 

```

## Notas adicionales

## Referencias

CYBERCHEF

