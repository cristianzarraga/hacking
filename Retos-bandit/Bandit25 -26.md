## Objetivo

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
- Usuario: **bandit25

## Solución

Para obtener la bandera de este nivel primero debemos abrir la terminal en el nivel 25 y posteriormente debemos ajustar la pantalla para que la información se vea mas estrecha, posteriormente ejecutaremos el siguiente comando:

ssh -i bandit26.sshkey bandit26@localhost -p 2220

ya que en el directorio raiz existe una llave privada llamada bandit26.sshkey, en caso de no ajustar la pantalla, el comando se ejecuta y la ventana se cierra de inmediato, al momento de estrechar la consola, al parecer no alcanza a cargar toda la info y se queda en algun modo de "standby" posteriormente presionamos la tecla V para entrar en VIM y poder ejecutar otro comando para visualizar la bandera, el comando es

```
:r /etc/bandit_pass/bandit26
```

```
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```


## Notas adicionales

Vim es un editor de texto y tenemos que desencadenar MORE, para poder visualizar la contraseña

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
[cron (Unix) - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cron_(Unix))