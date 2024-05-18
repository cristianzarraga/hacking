## Objetivo

This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/507/asciiftw).
## Solución

Utilizamos GHIDRA para poder resolver este reto

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cat data.txt | cut -d "," -f2 | xxd -r -p
picoCTF{ASCII_IS_EASY_7BCD971D} 
```

```
picoCTF{ASCII_IS_EASY_7BCD971D}
```


## Notas adicionales


## Referencias
