## Objetivo
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/56816/` ([link](https://jupiter.challenges.picoctf.org/problem/56816/)) or http://jupiter.challenges.picoctf.org:56816

## Solución

```
var a=['37115}','_again_3','this','Password\x20Verified','Incorrect\x20password','getElementById','value','substring','picoCTF{','not_this'];
undefined
a[8] + a[9] + a[2] + a[1] +a[0]
'picoCTF{not_this_again_337115}'

```

```
picoCTF{not_this_again_337115}
```


## Notas adicionales

Explorar en el código fuente
El codigo esta ofuscado y entramos a la consola del navegar haciendo observacion en la variable
HHTP Headers
Cambiar las Cookies

## Referencias
[Introducción a los archivos robots.txt | Centro de la Búsqueda de Google  |  Documentación  |  Google for Developers](https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es)