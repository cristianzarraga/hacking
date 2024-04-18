## Objetivo

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).
## Datos de acceso
## Solución

Utilizamos el comando steghide que nos ayudara a des encriptar la información, posteriormente utilizamos una web que realiza la decodificación para el texto en código Atbash

```
czarragar-picoctf@webshell:~$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
czarragar-picoctf@webshell:~$ 
czarragar-picoctf@webshell:~$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_7142uwv9}
```

```
picoCTF{atbash_crack_7142fde9}
```
## Notas adicionales 

## Referencias