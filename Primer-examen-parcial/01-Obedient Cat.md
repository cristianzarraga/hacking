## Objetivo
This file has a flag in plain sight (aka "in-the-clear").
## Datos de acceso
## Solución

````
````
```
czarragar-picoctf@webshell:~$ ls -la
total 20
drwxr-xr-x 2 czarragar-picoctf czarragar-picoctf   75 Feb 26 18:19 .
drwxr-xr-x 3 root              root                31 Feb 26 18:19 ..
-rw-r--r-- 1 czarragar-picoctf czarragar-picoctf  220 Feb 26 18:19 .bash_logout
-rw-r--r-- 1 czarragar-picoctf czarragar-picoctf 3771 Feb 26 18:19 .bashrc
-rw-r--r-- 1 czarragar-picoctf czarragar-picoctf  807 Feb 26 18:19 .profile
-rw-r--r-- 1 root              root              4443 Feb 26 18:19 README.txt
czarragar-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
--2024-02-26 18:20:40--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                       100%[======================================================================================================================================>]      34  --.-KB/s    in 0s      

2024-02-26 18:20:40 (16.6 MB/s) - 'flag' saved [34/34]

czarragar-picoctf@webshell:~$ ls
README.txt  flag
czarragar-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_2aa22101}
czarragar-picoctf@webshell:~$ 
```
## Notas adicionales

Aprendi a utilizar el comando wget

## Referencias