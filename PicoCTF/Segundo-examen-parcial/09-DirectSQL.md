## Objetivo

Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Solución

Nos conectamos a la base de datos y posteriormente exploramos, para poder realizar una consulta dentro de la base de datos que nos regresa la bandera

```
czarragar-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 57922 -U postgres pico
Password for user postgres: 
psql (14.11 (Ubuntu 14.11-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# /dt
pico-# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico-# select * public.flags
pico-# select * from public.flags
pico-# ^C
pico=# select * from public.flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 
```

## Notas adicionales


## Referencias
