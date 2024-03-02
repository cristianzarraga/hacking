## Objetivo

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## Solución

La evaluación if era incorrecta, era necesario agregar doble signo de = ya que solo tenia 1, dando la bandera correcta ahora

```
czarragar-picoctf@webshell:~$ ls
Addadshashanammu  README.txt  fixme2.py  output.txt  strings
czarragar-picoctf@webshell:~$ python3 fixme2.py 
  File "/home/czarragar-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
czarragar-picoctf@webshell:~$ nano fixme2.py
czarragar-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
czarragar-picoctf@webshell:~$ 
```

## Notas adicionales


## Referencias


