## Objetivo

Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/b44842413a0834f4a3619e5f5e629d05/shark1.pcapng).
## Solución

Descargamos el archivo y lo analizamos en Wireshark explorando al interior nos encontramos algo parecido a la bandera, la cual debemos de decodificar cvpbPGS{c33xno00_1_f33_h_qrnqorrs}, usando cyberchef obtenemos la bandera al aplicarle ROT13

```
picoCTF{p33kab00_1_s33_u_deadbeef}
```


## Notas adicionales

Utilizamos wireshark en kali
## Referencias
