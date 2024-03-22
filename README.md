# Analisis-y-Segmentacion-de-Clientes

## Descripción del conjunto de datos: 
Este conjunto de datos fue proporcionado por MiBanco en un taller de puesta en práctica de habilidades en Ciencia de Datos y Análisis de Datos. 

El conjunto de datos consiste en información sobre las compras de barras de chocolate de 500 personas de un área determinada cuando ingresan a una tienda física de "bienes de consumo masivo" en el período de 2 años. Todos los datos se han recopilado a través de las tarjetas de fidelización que utilizan al momento de pagar. Los datos se han procesado previamente y no faltan valores. Además, el volumen del conjunto de datos se ha restringido y anonimizado para proteger la privacidad de los clientes.

## Descripción de las variables en los datos: 
-	ID: Variable numérica. Muestra un identificador único de un cliente.
-	DIA: Variable numérica. Día en el que el cliente ha visitado la tienda (contado a partir del primer día del periodo de 2 años.
-	INCIDENCIA: Variable categórica. Es la incidencia de compra, 0 indica que el cliente no ha comprado un artículo de la categoría de interés y 1 que sí la ha comprado.
-	MARCA: Variable categórica. Indica cuál de las 5 marcas ha comprado el cliente. 0 indica que no compró ninguna marca.
-	CANTIDAD: Variable numérica. Número de artículos comprados por el cliente de la categoría de producto de interés.
-	ULTIMA_VENTA_MARCA: Variable categórica. Muestra cuál de las 5 marca ha comprado el cliente en su visita anterior a la tienda. 0 indica que no compró ninguna marca. 
-	PRECIO_1: Variable numérica. Precio de un artículo de la marca 1 en un día en particular
-	PRECIO_2: Variable numérica. Precio de un artículo de la marca 2 en un día en particular
-	PRECIO_3: Variable numérica. Precio de un artículo de la marca 3 en un día en particular
-	PRECIO_4: Variable numérica. Precio de un artículo de la marca 4 en un día en particular
-	PRECIO_5: Variable numérica. Precio de un artículo de la marca 5 en un día en particular
-	PROMOCION_1: Variable categórica. Indicador de si la Marca 1 estuvo o no en promoción en un día en particular.
-	PROMOCION_2: Variable categórica. Indicador de si la Marca 2 estuvo o no en promoción en un día en particular.
-	PROMOCION_3: Variable categórica. Indicador de si la Marca 3 estuvo o no en promoción en un día en particular.
-	PROMOCION_4: Variable categórica. Indicador de si la Marca 4 estuvo o no en promoción en un día en particular.
-	PROMOCION_5: Variable categórica. Indicador de si la Marca 5 estuvo o no en promoción en un día en particular.
-	SEXO: Variable categórica. Sexo del cliente 0 para masculino, 1 para femenino.
-	ESTADO_CIVIL: Variable categórica. 0 para soltero, 1 para no soltero (divorciado, separado, casado, viudo)
-	EDAD: Variable numérica. La edad del cliente en años, calculada como el año actual menos el año de nacimiento del cliente en el momento de la creación del conjunto de datos.
-	EDUCACIÓN: Variable categórica. 3 para escuela de posgrado, 2 para Universitarios, 1 para Escuela Secundaria, y 0 para desconocido u otro.
-	INGRESO: Variable numérica. Ingresos anuales auto informados en soles del cliente.
-	OCUPACIÓN: Variable categórica. 0 para desempleados, 1 para empleado, 2 para gerentes o empleados altamente calificados.
-	TAMAÑO_CIUDAD: Variable categórica. 0 para pequeña ciudad, 1 para ciudad mediana, 2 para gran ciudad.
  
## Conjunto de acciones realizadas en medio de la analítica de datos:
1.	Se realizó una exploración visual de las variables demográficas (sexo, estado civil, edad, educación, ingreso, ocupación y tamaño de ciudad).
2.	Se calcularon las siguientes variables por cada cliente: Recencia, que son los días desde la última venta efectiva para cada cliente siendo el día actual el número 731; Frecuencia, que es la cantidad de ventas efectivas para cada cliente; y Valor Monetario, que es el valor total de las ventas efectivas para cada cliente.
3.	Se definieron puntos de corte a criterio propio para cada una de las 3 variables mencionadas: Recencia, Frecuencia y Valor Monetario. De tal modo que se crearon 7 segmentos a partir de las combinaciones entre estas variables. Se determinó un número de 7 segmentos a partir del método del codo en el algoritmo de aprendizaje no supervisado: K-Means. De este modo es el algoritmo implementado el que determina las agrupaciones para posteriormente analizarlas y obtener insights a partir de ellas.
4.	Se interpretó cada segmento y se le puso un nombre de modo que fue posible identificar características útiles acerca de los clientes en estos 7 segmentos.
5.	Se obtuvieron otros 4 insights de importancia: Porcentaje del valor monetario que cada marca da a la empresa, Cantidad de productos Vendidos por cada marca; Precio promedio por Marca; y porcentajes de compras que se hicieron tras: bajar el precio del producto, subir el precio del producto, y mantener igual el precio del producto. 
6.	Se determinó qué segmentos podrían considerarse como “Clientes dormidos”, “Clientes potenciales”, y “Clientes en riesgo”.

## Exploración visual de las variables demográficas y gráficos de otros Insights

### Cantidad de clientes por edad:
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/57ffaf8b-37da-428d-8335-17b1916f332b)

### Cantidad de clientes de acuerdo a su rango de ingresos
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/e5505d18-2380-4a40-936b-c24207b98a72)

### Cantidad y porcentaje de clientes por sexo
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/6390d21c-e7c3-486b-b5d4-beb780a7e5d7)

### Porcentaje y cantidad de clientes por nivel educativo
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/7d7f9c7d-1c00-4bd3-9ad0-fe12b809a8bc)

### Porcentaje y cantidad de clientes dada su ocupación
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/f0831c91-190d-4caf-b5a5-94f3d15ef667)

### Porcentaje y cantidad de clientes dado el tamaño de sus ciudades
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/c11a8ace-12b6-4dbb-843f-bd7cb9554914)

### Porcentaje del valor monetario que cada marca da a la empresa
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/19777dba-2145-484a-8f29-d2db4f2c408a)

### Cantidad de productos vendidos por marca
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/11ba9a2b-b413-4139-a835-78491bf73d0a)

### Precio promedio por marcas
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/ba8085fe-17bb-495b-8865-913f44466ceb)

### Porcentajes de Compras que se hicieron tras: bajar el precio del producto, subir el precio del producto y mantener igual el precio del producto
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/b4049b2d-8d35-4cc2-bd90-497661c53b67)

## Explicación de los segmentos obtenidos de los clientes. Agrupaciones y descripciones de las mismas.

Segmento 0 – Clientes activos y potenciales: 
Medianamente numeroso número de clientes, con alto número de compras efectivas, aportan importante valor monetario a la empresa, muy baja recencia, alto número de visitas. De pequeñas y medianas ciudades, en su mayoría empleados y algunos gerentes, proporción importante de mujeres (más de la mitad), ingresos medios, en su mayoría bachilleres y varios universitarios, promedio de edades de 39 años, mitad solteros. 
Prefieren las marcas 2 y 4, reaccionan más a las promociones de la marca 2 y reaccionan en medida considerable a las promociones en general. 

Segmento 1 – Clientes de actividad-media-baja: 
Altamente numeroso número de clientes, es relativamente bajo el valor monetario que aportan a la empresa (segmentos que menos aporta al valor monetario), recencia relativamente baja, no muy alto número de visitas. De pequeñas ciudades en su mayoría, empleados y desempleados, segmento de más bajo ingreso y menor nivel educativo, en su mayoría bachilleres y pocos universitarios, segmento con promedio de edad más baja (36 años), en su mayoría solteros y con una proporción considerable de mujeres (44 %).
Prefieren la marca 2, reaccionan más a las promociones de la marca 2, y reaccionan en baja medida a las promociones.

Segmento 2 – Clientes de actividad media-baja: 
Medianamente numeroso, moderada cantidad de ventas efectivas, recencia relativamente alta, aportan mediana cantidad de Valor Monetario a la compañía (pero sigue siendo una cantidad de importancia), y mediana cantidad de visitas. En su mayoría de medianas ciudades, aunque también de pequeñas ciudades, en su mayoría empleados y algunos desempleados, ingresos medio-altos, segmento con mayor nivel educativo (universitarios en su mayoría, y algunos bachilleres), promedio de edad de 43 años y es el segmento con mayor número de personas No solteras. 
Prefieren la marca 4, aunque también gustan de la marca 1 y 2, y reaccionan más a las promociones de la marca 2. Relativamente baja reacción a las promociones.

Segmento 3 – Clientes muy activos y potenciales: 
No tan numeroso, alto número de ventas efectivas, alto valor monetario a la empresa, baja recencia, gran porcentaje de visitas que terminaron en ventas, alto número de visitas. Muchos de grandes ciudades, y otros de medianas ciudades, conformado por empleados y gerentes, alto nivel educativo (universitarios y bachilleres), ingresos altos, con un promedio de edades de 44 años y casi la mitad de las personas son solteras. 
Prefieran la marca 5 pero también les gusta la 4, y reaccionan más a las promociones de la marca 2. Reaccionan en gran medida a las promociones, son los que más compran en promociones. 

Segmento 4 – Clientes de alto riesgo: 
No muy alta cantidad de clientes, relativamente bajo el valor monetario aportado a la empresa, baja cantidad de ventas efectivas, alta recencia, cantidad de visitas medio-baja. De pequeñas y medianas ciudades, empleados y desempleados, ingresos medio, en su mayoría bachilleres y algunos universitarios, edad promedio de 39 años y un 32% de personas no solteras. 
Prefieren la marca 2 pero gustan de la marca 5, y reaccionan más a las promociones de la marca 2. Reaccionan muy poco a las promociones. 

Segmento 5 – Clientes dormidos:  
Numerosa cantidad de clientes, baja recencia, media-baja cantidad de ventas efectivas, bajo número de visitas (los que menos visitas hacen), no es muy alto el valor monetario que aportan a la compañía. De medianas y pequeñas ciudades, empleados en su mayoría y algunos gerentes, de ingreso medio, bachilleres y algunos universitarios, promedio de edad de 39 años, y un 40% de personas no solteras. 
Prefieren la marca 2, reaccionan más a las promociones de la marca 2. Reacción moderada a las promociones. 

Segmento 6 – Clientes en riesgo: 
Segmentos que menos valor monetario aporta a la empresa, no muy alta cantidad de clientes, alta recencia, baja cantidad de visitas. Vienen en su mayoría de medianas ciudades y algunos de pequeñas, Ingresos medio-bajos (relativamente), no muy alto nivel educativo (en su mayoría bachilleres) y algunos sin educación, promedio de edad de 37 años (segundo segmento más joven), 31% en estado civil de No soltería.
Prefieren la marca 2, aunque gustan de la 5 y reaccionan más a las promociones de la marca 2. Reacción baja a las promociones

Segmento 7 – Clientes Especiales:
Son los que más valor monetario dan a la compañía, muy bajo número de clientes (solo hay 8), con mayor cantidad de ventas efectivas registradas, de menor recencia, los que más visitas hacen. De grandes ciudades en su mayoría y otros de medianas, en su mayoría gerentes y algunos empleados, ingresos altos, en su mayoría universitarios y posgrados, edad promedio de 46 años (segmento de mayor edad), y es el que mayor número de personas solteras tiene. 
Prefieren la marca 5 y prefieren esta marca durante las promociones. Reaccionan altamente a las promociones.


