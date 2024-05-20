## GROUP BY

```
create table productos (
id serial primary key,
nombre varchar(100),
categoria varchar(50),
precio int
)

insert into productos (nombre, categoria, precio)
values
('Laptop', 'Computadores', 12000),
('Teléfono', 'Electrónica', 5000),
('Camiseta', 'Ropa', 560000),
('MacBook Pro', 'Computadores', 456000),
('Zapatos', 'Ropa', 542000),
('Libro', 'Libros', 4000);

select * from public.productos

select categoria, COUNT(*) as cantidad_productos from productos group by categoria;
```

## LIKE
```
select * from public.productos where nombre like '%Tel%'
```

## HAVING BY

```
select categoria, AVG(precio) as precio_promedio
from productos
group by categoria
having avg(precio) > 5000

select categoria, AVG(precio) as precio_promedio
from productos
group by categoria
having avg(precio) >= 234000
```

## DISTINCT

```
create table clientes(
id serial primary key,
nombre varchar(50),
ciudad varchar(20),
edad int
)

insert into clientes (nombre, ciudad, edad) values ('Daniel', 'Armenia', 60);
insert into clientes (nombre, ciudad, edad) values ('Ramiro', 'Armenia', 19);
insert into clientes (nombre, ciudad, edad) values ('Angel', 'Bogota', 28);
insert into clientes (nombre, ciudad, edad) values ('Felipe', 'Cali', 34);
insert into clientes (nombre, ciudad, edad) values ('Angela', 'Pereira', 45);

select * from public.clientes

select distinct ciudad from clientes
```
## ORDER BY

```
select * from clientes order by edad asc
select * from clientes order by edad desc

select * from clientes order by nombre asc
select * from clientes order by nombre desc

select * from clientes order by nombre,edad asc
```

## LIMIT

```
select * from clientes limit 3
select * from clientes order by id desc limit 3
```

## Documentacion:

https://www.postgresql.org/docs/16/reference.html

https://devdocs.io/

https://miro.com/es/diagrama/que-es-diagrama-uml/

https://www.lucidchart.com/pages/es

https://dbdiagram.io/home

