## Objetivo

We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/127/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Datos de acceso
## Solución


```
czarragar-picoctf@webshell:~$ cat message.txt 
128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140 czarragar-picoctf@webshell:~$ nano crypto.py  
czarragar-picoctf@webshell:~$ python3 crypto.py 
R0UND_N_R0UND_79C18FB3czarragar-picoctf@webshell:~$ 
```

```
picoCTF{R0UND_N_R0UND_79C18FB3}
```
## Notas adicionales 

## Referencias