## Objetivo
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...
## Solución

From charcode base 10
Utilizamos CyberChef para realizar la conversion.

```
czarragar-picoctf@webshell:~$ nc mercury.picoctf.net 35652
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
57 
98 
51 
98 
55 
51 
57 
50 
125 
10 
```

bandera: picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}
## Notas adicionales

- chmod +x warm - Asigna permisos de ejecucion a un archivo binario
- ./warm - Abre archivos

## Referencias