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
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
