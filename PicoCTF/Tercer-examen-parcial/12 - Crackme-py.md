## Objetivo

[crackme.py](https://mercury.picoctf.net/static/f440bf2510a28914afae2947749f2db0/crackme.py)
## Solución

Comentamos uno de los metodos en el codigo en python y nos arrojo directamente la bandera

```
 czarragar-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/f440bf2510a28914afae2947749f2db0/crackme.py
--2024-05-16 22:54:52--  https://mercury.picoctf.net/static/f440bf2510a28914afae2947749f2db0/crackme.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1463 (1.4K) [application/octet-stream]
Saving to: 'crackme.py'

crackme.py            100%[=======================>]   1.43K  --.-KB/s    in 0s      

2024-05-16 22:54:52 (890 MB/s) - 'crackme.py' saved [1463/1463]

czarragar-picoctf@webshell:~$ python3 crackme.py 
What's your first number? 3
What's your second number? 2
The number with largest positive magnitude is 3
czarragar-picoctf@webshell:~$ nano crackme.py 
czarragar-picoctf@webshell:~$ python3 crackme.py 
picoCTF{1|\/|_4_p34|\|ut_8c551048}
czarragar-picoctf@webshell:~$ ^C
czarragar-picoctf@webshell:~$ 
```

```
picoCTF{1|\/|_4_p34|\|ut_8c551048}
```


## Notas adicionales


## Referencias
