## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...
## Solución

````
````
```
czarragar-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
--2024-02-26 18:29:09--  https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                       100%[======================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2024-02-26 18:29:09 (312 MB/s) - 'warm' saved [10936/10936]

czarragar-picoctf@webshell:~$ ls
README.txt  flag  warm
czarragar-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
czarragar-picoctf@webshell:~$ chmod +x warm
czarragar-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
czarragar-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
czarragar-picoctf@webshell:~$ 
```
## Notas adicionales

- chmod +x warm - Asigna permisos de ejecucion a un archivo binario
- ./warm - Abre archivos

## Referencias