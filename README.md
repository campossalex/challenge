# SEBC Final Challenge

Bienvendio al Desafío Final del Bootcamp Cloudera 

Usted deberá crear un pipeline completo, ingestando datos de una base de datos y archivos de access log de Apache. La idea es relacionar la información de navegación de la página web con las transacciones de ventas. 

1. Ingestar datos de las transacciones de ventas:  
IP: 34.205.65.241  
Puerto: 3306  
Usuario: bootcamp  
Contraseña: bootcamp  
Base de datos: ecommerce  
Tabla: product_transaction  
Motor: MySQL  

2. Logs de acceso de Apache Web Server:  

3. Regex para SerDe en Hive:  
`^(\\S+) \\S+ \\S+ \\[([^\\[]+)\\] "(\\w+) (\\S+) (\\S+)" (\\d+) (\\d+) "([^"]+)" "([^"]+)".*`  

## Objetivo:

Calcular la conversión de venta de cada sku.  
Fórmula conversión de venta: ventas por producto / visualización producto  

La visualización de los productos se hace por medio de la siguiente página web:  
/item/id?skuID=
