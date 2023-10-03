# consultas_1_SQL
# Introducción a las consultas en una base de datos en sql

## Base de datos: Ventas
## Tabla: Cliente

![Tabla Cliente](./img/ejemplo1.png.png "Tabla Cliente")

## Instruccion SELECT
- Permite seleccionar datos de una tabla.
- Su formato es: `SELECT campos_tabla FROM nombre_tabla``

### CONSULTA No. 1
1. Para visualizar toda la informacion que contiene la tabla Cliente se puede incluir con la instruccion SELECT el caracter **\*** o cada uno de los campos de la tabla.

- `SELECT * FROM Cliente`
![Consulta](./img/cliente1_1.png "Tabla consulta1_2")
- `SELECT identificacion, nombre, apellidos,direccion, telefono, ciudad_nac, fecha_nac FROM Cliente`
![Tabla Cliente](consulta1_2.png "Tabla consulta 2")

### Consulta No. 2

2. Para visualizar solamente la identificacion del Cliente: `SELECT identificacion FROM Cliente`
![Tabla Cliente](./img/consulta2.png "Tabla consulta 2")

### Consulta No. 3

3. Si se desea obtener los registros cuya identificacion sea mayor o igual a 150, se debe utilizar la clausula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * FROM Cliente WHERE Idetificación>=150`
![Tabla Cliente](./img/consulta3.png "Tabla consulta 3")


### Consulta No. 4

4. Se desea obtener los registros cuyos apellidos sean Vanegas o Cetina, se debe utilizar el operador `IN` que especifica los registros que se quieren visualizar de una tabla.

`SELECT apellido, FROM Cliente WHERE apellido IN('Vanegas', 'Cetina')`
![Tabla Cliente](./img/consulta4_1.png "Tabla consulta 4_1")


o se puede utilizar el operador `OR`

`SELECT apellido,Nombre FROM Cliente WHERE apellido = 'Vanegas' OR apellido = 'Cetina'`
![Tabla Cliente](./img/consulta4.png "Tabla consulta 4_2")

### Consulta No.5

5. Se desea obtener los registros cuya identificacion sea menor de 110 y la ciudad sea Cali, se debe utilizar el operador `AND`

`SELECT * FROM Cliente WHERE identificion<=110 AND ciudad = 'Cali'`

![Consulta](./img/consulta5.png "consulta 5")


### Consulta No.6 

6. Si se desea obtener los registros cuyos nombres empiecen por la letra `A`, se debe utilizar el operador `LIKE` que utiliza los patrones `%` (todos) y `_` (caracter). 

`SELECT * FROM Ventas WHERE Nombre LIKE 'A%'`

![Consulta](./img/consulta6.png "consulta 6")

### Consulta No.7 
7. Se desea obtener los registros cuyos nombres contengan la letra 'a'
`SELECT * FROM Ventas WHERE Nombre Like '%a%'`

![Consulta](./img/consulta7.png "consulta 7")

### Consulta No.8
8. Se desea obtener los registros donde la cuarta letra del nomnre del cliente sea la letra 'a'

`SELECT * FROM Ventas WHERE Nombre LIKE '___a'`
![Consulta](./img/consulta8.png "consulta 8")

### Consulta No.9
9. Si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se debe utilizar la clasula `BETWEEN`, que sirve para especificar un intervalo de valores 
`SELECT * FROM Ventas WHERE identificacion BETWEEN 110 AND 150`
![Consulta](./img/consulta9.png "consulta 9")

## Instruccion DELETE
- Permite borrar todos o un grupo especifico de una tabla.
- Su formato es: `DELETE FROM nombre_tabla`

### Eliminación No.1

1. Eliminar los registros cuya identificacion sea mayor a 170.

`DELETE FROM Ventas WHERE identificacion > 9635561`
![delte](./img/delete1.png "delete 1")
Se elimino a Juan Santana Ruiz

2. Eliminar los registros cuya identificacion sea igual a 116
`DELETE FROM Ventas WHERE identificacion = 116`

## Instruccion UPDATE
- Permite actualizar un campo de tabla.
- Su formato es: `UPDATE nombre_tabla SET nombre_campo = valor`

### Actualización 
1. Para actualizar la ciudad de nacimiento de Cristian Vanegas, cuya identificacion es 114
`UPDATE Ventas SET ciudad_nac = 'Pereira' WHERE identificacion=114`
![update](./img/update1.png "update 1")