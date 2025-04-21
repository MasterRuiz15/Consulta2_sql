# Consulta2_sql
![Consulta 1](imagen/Empresa.png  "Consulta 1")

![Consulta 2](imagen/Tabla_Departameno.png  "Consulta 2")

![Consulta 3](imagen/Empleados.png  "Consulta 3")

1. Obtener la lista de los apellidos de todos los empleados.

` SELECT apellidos_empleados FROM Empleados; `

![Consulta 1](imagen/Apellidos.png  "Consulta 1")

2. Obtener la lista de los apellidos de todos los empleados.

` SELECT apellidos_empleados FROM Empleados; `

![Consulta 2](imagen/Apellidos.png  "Consulta 2")

3. Obtener los apellidos de todos los empleados sin repeticiones.

`SELECT nombre_empleados FROM Empleado;`

![Consulta 3](imagen/Apellidos.png  "Consulta 3")

4. Obtener todos los datos de los empleados que se apellidan 'Gomez'.

`SELECT * FROM Empleado WHERE apellidos_empleados = 'Gomez';`

![Consulta 4](imagen/4.png  "Consulta 4")

5. Obtener todos los datos de los empleados que se apellidan "Diaz" y los que se apellidan "Rodriguez".  Usar OR o IN

`SELECT * FROM Empleado WHERE apellidos_empleados IN ('Diaz', 'Rodriguez');`

![Consulta 5](imagen/5.png  "Consulta 5")

6. Obtener los nombres de los empleados que trabajan en el departamento 11

`SELECT nombre_empleado FROM Empleado WHERE id_departamento = 11;`

![Consulta 6](imagen/6.png  "Consulta 6")

7. Obtener todos los datos de los empleados cuyo apellido empiece por 'P'

`SELECT * FROM Empleado WHERE apellidos_empleados LIKE 'P%';`

![Consulta 7](imagen/7.png  "Consulta 7")

8. Obtener el presupuesto total de todos los departamentos.

`SELECT SUM(presupuesto_departamento) AS presupuesto_total FROM Departamento;`

![Consulta 8](imagen/8.png  "Consulta 8")

9. Obtener el número de empleados de cada departamento.

`SELECT id_departamento, COUNT(*) AS cantidad_empleados FROM Empleado GROUP BY id_departamento;`

![Consulta 9](imagen/9.png  "Consulta 9")

10. Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado y de su departamento.

`SELECT * FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento;`

![Consulta 10](imagen/10.png  "Consulta 10")

11. Obtener un listado completo de empleados, incluyendo el nombre y apellidos del empleado junto al nombre y presupuesto de su departamento.

`SELECT Empleado.*, Departamento.* FROM Empleado JOIN Departamento ON Empleado.id_departamento = Departamento.id_departamento;`

![Consulta 12](imagen/11.png  "Consulta 12")

12. Obtener los nombres y apellidos de los empleados que trabajen en departamentos cuyo presupuesto sea mayor a 100000000

`SELECT Empleado.nombre_empleado, Empleado.apellidos_empleados FROM Empleado JOIN Departamento ON Empleado.id_departamento = Departamento.id_departamento WHERE Departamento.presupuesto_departamento > 100000000;`

![Consulta 12](imagen/12.png  "Consulta 12")
