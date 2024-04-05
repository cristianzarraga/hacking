## Objetivo

Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/124/anthem.flag.txt).
## Solución

Descargamos el archivo, realizamos un cat y con un grep para identificar la bandera entre todos los datos


```
czarragar-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/124/anthem.flag.txt--2024-04-05 18:08:58--  https://artifacts.picoctf.net/c/124/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: 'anthem.flag.txt'

anthem.flag.txt       100%[=======================>] 106.12K  --.-KB/s    in 0.005s  

2024-04-05 18:08:58 (19.5 MB/s) - 'anthem.flag.txt' saved [108668/108668]

czarragar-picoctf@webshell:~$ ls
README.txt  anthem.flag.txt  cat.jpg  filler.txt  flag.png  moonwalk  whitepages.txt
czarragar-picoctf@webshell:~$ cat anthem.flag.txt | grep pico
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}
```


## Notas adicionales


## Referencias
