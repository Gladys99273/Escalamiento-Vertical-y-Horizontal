# Escalamiento-Vertical-y-Horizontal
*Escalamiento Vertical (Escalado vertical del plan de tarifa)
1.- En el explorador, vamos a buscar Azure Portal. Y nos creamos una cuenta
2.- En el menú de la izquierda de la página de la aplicación de App Service,
seleccione Escalar verticalmente (plan de App Service) .
3.-Elijimos el nivel (son del cuadro naranja F1 infraestructura
compartidas 1gb memoria 60 minutos al dia de computo gratis ----
D1 infraestructura compartidas 1gb memoria 240 minutos al dia de
computo gratis ---- b1 1.75 gb memoria )y, después, seleccione Aplicar.
Seleccione de entre las distintas categorías desarrollo/ prueba -----
producción ---- aislado (por ejemplo, Producción) y al final le damos clic
en aplicar
Una vez completada la operación, aparecerá una ventana emergente de
notificación con una marca de verificación verde de operación correcta.
4.- en este caso vamos a la información general de la aplicaciones y seleccionamos el vinculo
grupo de recursos
Al momento de dar clic aparecerá esta pantalla y aquí podemos seleccionar el recurso que
queremos escalar en este caso queremos escalar el segundo que es coreDB

*Escalamiento Horizontal(Implementación de balance de carga )

1- Ingresamos a nuestra cuenta de aws
2- Damos clic en ec2
3- Y nos vamos a la parte izquierda del menú y buscamos balanceador y damos
clic en crear
4- Y nos va aparecer esta pantalla que estamos visualizando en estos momentos
5- En el name vamos a escribir el nombre del balanceadorPrueba
6- Y en el esquema si se esta usando el sistema para el publico utilizamos
exposed to the internet ,pero si el sistema solo se utiliza de forma interna se
usaría internal
7- En este caso vamos a seleccionar exposed to the internet
8- Y en el tipo de dirección de ip lo dejamos en ipv4
9- Después nos vamos a donde dice protocolo del equilibrador de carga (load
balance protocol) y seleccionamos en TCP (protocolo de control de
transmisión )
10- Después nos vamos a puerto del equilibrador de carga (load balancer port) y
nos colocamos en el puerto 80 
11. acontinuacion tenemos la disponibilidad es decir las zonas disponibles en la
cual va a trabajar
12. seleccionamos en availitar zonas y damos clic en sgte
13. en el sgte paso vemos targer group seleccionamos new trager group(nuevo objetivo de
grupo )
14.- creamos el nombre del grupo de seguridad que se llamará Balance1
15. y en el tipo de destino tenemos dos opciones que serian instancia o una Ip
16. en este caso seleccionaremos la IP
17. en este caso nuestro protocolo será tcp
18.- y nuestro puerto será de 80y le damos clic en el sgte registro de destino
19.- el sgte paso seleccionamos nuestra red
20.- se tiene que digitar la ip
21.- la ip es la cual va a ingresar en el balanceador de carga y esta ya fue creada previamente
22.- nuestro puerto sera de 80 y le damos clic en sigte 
23.- en esta pantalla veremos los detalles del balanceador de carga que se a creado
24.- veamos que todo este bien y le damos clic en crear
25.-y tendríamos nuestro balanceador creado y nos mostrará este mensaje que se a creado
correctamente
