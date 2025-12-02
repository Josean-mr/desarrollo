[Transacciones en MySQL](https://basmoxo.wordpress.com/wp-content/uploads/2011/10/transacciones-ii.pdf)
<font style="color:green">Ejemplo:</font>
- Crea una transacción en la que, sobre la tabla empleados, incrementes en 100 el salario del empleado con ID = 4 y reduzcas en 100 el salario del empleado con ID = 8. Por último, deshaz los cambios para finalizar la transacción.
 ```sql
START TRANSACTION;

UPDATE empleados
SET Salario = Salario + 100
WHERE ID_Empleado = 4;

UPDATE empleados
SET Salario = Salario - 100
WHERE ID_Empleado = 8;

ROLLBACK;
```
