<h1>Aplicar filtros para consultas Sql lab</h1

<h2>Description</h2> 

Soy un profesional de la seguridad en una gran organización. Parte de mi trabajo consiste en investigar problemas de seguridad para ayudar a mantener la seguridad del sistema. Recientemente he descubierto algunos posibles problemas de seguridad relacionados con intentos de inicio de sesión y equipos de empleados.
Mi tarea consiste en examinar los datos de la organización en las tablas employees y log_in_attempts. Tengo que utilizar filtros SQL para recuperar registros de diferentes conjuntos de datos e investigar los posibles problemas de seguridad.



<br />


<h2>Languages </h2>

- <b>Sql </b> 
  

<h2>Environments Used </h2>

- <b>Linux</b> 

<h2>Recorrido por el programa :</h2>


Para recuperar los intentos de inicio de sesion fallidos ocurridos después de las horas laborales '18:00:00'), la correcta consulta es:
<img src=https://i.imgur.com/W1GpXhZ.png


<img src=https://i.imgur.com/W1GpXhZ.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
Explicacion:
login_time > '18:00:00':  Filtra los intentos de inicio de sesion ocurridos después de 6:00pm horas de oficina terminadas
success = 0: filtra por intentos de inicios de sesion fallidos     0 representa FALSE no exitoso.
SELECT *Recupera todas las columnas de log_in_attempts table  de  los registros que coinciden.

 <br/>Recuperar intentos de inicio de sesión en fechas concretas.: <br/>
<img src=https://i.imgur.com/4g1Trnj.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>Explicacion:
SELECT *: Recupera todas las columnas de   log_in_attempts table  de los registros que coinciden 
login_date = '2022-05-08' OR login_date = '2022-05-09': Filtra los resultados que incluyen los intentos de inicio de sesion sean  May 8, 2022, or May 9, 2022.

<br />Recuperar intentos de inicio de sesión fuera de México
<br/>
<img src=https://i.imgur.com/anx7ylZ.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />SELECT *: Recupera toda las columnas de  log_in_attempts table  de los intentos de inicio de sesion no originados en Mexico
 NOT:  Garantiza la condition es invertida , es decir excluira los registros que coinciden con el patron 'MEX%'.
LIKE 'MEX%': Iguala cualquier valor en la columna country que empiece con 'MEX' (cubriendo ambos 'MEX' and 'MEXICO').

<br/>Recuperar empleados en finanzas o ventas
<img src=https://i.imgur.com/y15fAid.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>Explicación:
<br />SELECT *:Recupera todas las columnas de la tabla employees para los registros que coinciden con cualquiera de las dos condiciones.
department = 'Finance': Filtra los empleados que pertenecen al departamento de Finance.
OR: Especifica que se debe cumplir una de las dos condiciones, es decir, pertenecer a cualquiera de los dos departamentos.
department = 'Sales': Filtra los empleados que pertenecen al departamento de Sales.
 
  <br/>

  <br/> Recuperar todos los empleados no esten en it 

<img src=https://i.imgur.com/4xkeHzJ.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />Explicación
<br />SELECT *: Recupera todas las columnas de la tabla employees para los registros que cumplen con la condición de no estar en el departamento de Information Technology.
NOT department = 'Information Technology': Esta condición excluye a los empleados que pertenecen al departamento de Information Technology.
  <br/>

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
