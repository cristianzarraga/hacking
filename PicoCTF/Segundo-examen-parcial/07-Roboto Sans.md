## Objetivo

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:59901/) out.
## Solución

Exploramos el archivo robots.txt, donde nos da un codigo al parecer en base 64, al decodificar la segunda linea nos da un path js/myfile.txt, al ingresarla junto con la URL, nos regresa de respuesta la bandera

```
picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
```

## Notas adicionales


## Referencias
