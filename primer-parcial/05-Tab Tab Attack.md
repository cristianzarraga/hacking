## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)
## Solución

Utilizamos el unzip para descomprimir el archivo el cual genera varias carpetas, accedemos hasta la final y encontramos un ejecutable
```
czarragar-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 53914
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Mon Feb 26 19:12:05 2024 from 127.0.0.1
ctf-player@pico-chall$ 
ctf-player@pico-chall$ 
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ 
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cd 3of3.flag.txt 
-bash: cd: 3of3.flag.txt: Not a directory
ctf-player@pico-chall$ cat 3of3.flag.txt 
c1754242}
ctf-player@pico-chall$ 
```

bandera: picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}
## Notas adicionales

- chmod +x warm - Asigna permisos de ejecucion a un archivo binario
- ./warm - Abre archivos

## Referencias