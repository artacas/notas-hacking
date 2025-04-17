## Descripción:
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 59318 -U postgres pico`Password is `postgres`

Hints:
What does a SQL database contain?

## Solución:
```
artacas-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 59318 -U postgres pico
Password for user postgres: 
psql (14.17 (Ubuntu 14.17-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# \d
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# \d flags
                        Table "public.flags"
  Column   |          Type          | Collation | Nullable | Default 
-----------+------------------------+-----------+----------+---------
 id        | integer                |           | not null | 
 firstname | character varying(255) |           |          | 
 lastname  | character varying(255) |           |          | 
 address   | character varying(255) |           |          | 
Indexes:
    "flags_pkey" PRIMARY KEY, btree (id)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
```

## Notas:


