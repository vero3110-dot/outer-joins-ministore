# outer-joins-ministore

Práctica realizada en sql server

¿Por qué usaste LEFT JOIN para la Consulta 1 y no INNER JOIN? ¿Qué se perdería si usaras INNER JOIN?
use Left join porque ubique la tabla de productos a la izquierda y asi podria ver de todos esos productos cuales quedan sin ventas, ya que el left join mantiene todos los registros en el resultado aunque no tengan contrapartida en la tabla de la derecha. Si usara inner join esos registros se perderian y solo quedarian los que tienen contrapartida.

¿Por qué usaste RIGHT JOIN para la Consulta 2? ¿Qué tabla está a la izquierda y cuál a la derecha en tu consulta?
En la consulta 2 utilice la misma ubicacion de las tablas en el join pero utilice right join para dejar todas las filas de la tabla 2 que estaba a la derecha y es la tabla ventas. A la izquierda deje la tabla productos. De esta forma puedo ver si hay algun registor de la tabla ventas que no tiene completo los campos de la tabla producto.

¿Qué representan los valores NULL en cada resultado? Explicá con un ejemplo concreto de los datos qué significa que venta_id sea NULL en la Consulta 1 y que producto_id de productos sea NULL en la Consulta 2.
Que venta_id sea null para un producto significa que este nunca tuvo una venta. 
Que producto_id sea null en la consulta 2 significa que ese campo no se completo en la operacion de venta registrada

¿Cuándo usarías FULL OUTER JOIN en un caso real de negocio?
En estas tablas seria util para tener la base completa de registros y no perder de vista ningun producto existente y ninguna venta (lo cual da consistencia con otros reportes sumarizados). Al analizar la base completa se pueden identificar mejoras en los procesos para contar con datos completos.
