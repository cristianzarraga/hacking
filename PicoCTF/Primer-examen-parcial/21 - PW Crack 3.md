## Objetivo

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

Tuvimos que crear un for al final del archivo para comprobar cual era el password correcto y poder ingresarlo


```
czarragar-picoctf@webshell:~$ ls
README.txt  level3.flag.txt.enc  level3.hash.bin  level3.py
czarragar-picoctf@webshell:~$ nano level3.py 
czarragar-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: r
That password is incorrect
2295
czarragar-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
2295
czarragar-picoctf@webshell:~$  

```

## Notas adicionales

## Referencias

CYBERCHEF

