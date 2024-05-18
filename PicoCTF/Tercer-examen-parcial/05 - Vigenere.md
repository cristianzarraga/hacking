## Objetivo

Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/158/cipher.txt) using this key "CYLAB".
## Solución

Utilizamos un decodificador online

```
czarragar-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/158/cipher.txt
--2024-04-26 22:53:39--  https://artifacts.picoctf.net/c/158/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: 'cipher.txt'

cipher.txt            100%[=======================>]      43  --.-KB/s    in 0s      

2024-04-26 22:53:39 (17.7 MB/s) - 'cipher.txt' saved [43/43]

czarragar-picoctf@webshell:~$ cat cipher.txt 
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_cc82272b}
czarragar-picoctf@webshell:~$ 
```

```
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_ae82272q}
```


## Notas adicionales


## Referencias
