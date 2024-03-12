# Analisis-y-Segmentacion-de-Clientes

## Descripción del conjunto de datos: 
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
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/37f3c2f6-dc50-4026-9237-399089e8ef56)

### Cantidad de clientes de acuerdo a su rango de ingresos
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/b306ca35-9363-4bf9-9c8c-cbc77775e941)

### Cantidad y porcentaje de clientes por sexo
![Picture1](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/ff34ce7c-f305-4fbc-9262-f1f929317c7a)

### Porcentaje y cantidad de clientes por nivel educativo
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/b14914f6-5e7a-476c-95b4-c1e647113550)

### Porcentaje y cantidad de clientes dada su ocupación
![Picture2](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/72f28865-0f22-4f92-8ede-5d3b07b88012)

### Porcentaje y cantidad de clientes dado el tamaño de sus ciudades
![Picture3](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/2631db63-d3b3-4bbe-bc31-81251a67279a)

### Porcentaje del valor monetario que cada marca da a la empresa
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/f094908b-592d-458c-9773-c9c7f3dec84d)

### Cantidad de productos vendidos por marca
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/f1abb913-0a02-4727-a5a3-0764636981cb)

### Precio promedio por marcas
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/bfa31fd6-ebf1-4da5-819e-3df35c17df9f)

### Porcentajes de Compras que se hicieron tras: bajar el precio del producto, subir el precio del producto y mantener igual el precio del producto
![image](https://github.com/DanielAndres1116/An-lisis-y-Segmentaci-n-de-Clientes/assets/43154438/3df74886-5847-4b02-8a7d-bd59a957e2f5)


