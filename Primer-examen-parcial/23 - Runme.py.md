## Objetivo

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución

Para este desafío solo tuvimos que correr el archivo con python3 runme.py


```
czarragar-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2024-03-01 23:14:13--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                                   100%[======================================================================================================================================>]     270  --.-KB/s    in 0s      

2024-03-01 23:14:14 (12.7 MB/s) - 'runme.py' saved [270/270]

czarragar-picoctf@webshell:~$ ls
runme.py
czarragar-picoctf@webshell:~$ python3 runme.py 
picoCTF{run_s4n1ty_run}
czarragar-picoctf@webshell:~$  

```

## Notas adicionales

## Referencias

CYBERCHEF

