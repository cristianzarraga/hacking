## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución

le hicimos un Cat al archivo descargar FILE en el cual, vimo mucha informacion desordenada y posteriormente hicimos un grep para visualizar o filtrar lo que nos interesa

```
czarragar-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  code.py  codebook.txt  convertme.py  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  warm
czarragar-picoctf@webshell:~$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_dba08a45}
czarragar-picoctf@webshell:~$ 

```

## Notas adicionales

cat File | grep pico

Convertir de decimal a binario
## Referencias

Calculadora de decimal a binario