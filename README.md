# SEBC Final Challenge

Bienvendio al Desafío Final del Bootcamp Cloudera. Lograste llegar a la última etapa :)  

Usted deberá crear un pipeline completo, ingestando datos de una base de datos y archivos de access log de Apache. La idea es relacionar la información de navegación de la página web con las transacciones de ventas. 

1. Ingestar datos de las transacciones de ventas:  
IP: 34.205.65.241  
Puerto: 3306  
Usuario: bootcamp  
Contraseña: bootcamp  
Base de datos: ecommerce_cloudera  
Tabla: product_transaction  
Motor: MySQL  

2. Logs de acceso de Apache Web Server:  
http://34.205.65.241/access.log  
Columnas para tabla de logs: ip, time_local, method, uri, protocol, status, bytes_sent, referer, useragent  
<!-- SerDe class: org.apache.hadoop.hive.serde2.RegexSerDe -->

3. Regex para SerDe en Hive:  
`^(\\S+) \\S+ \\S+ \\[([^\\[]+)\\] "(\\w+) (\\S+) (\\S+)" (\\d+) (\\d+) "([^"]+)" "([^"]+)".*`  

4. Exportar la convesión por producto a una tabla:  
IP: 34.205.65.241  
Puerto: 3306  
Usuario: bootcamp  
Contraseña: bootcamp  
Base de datos: ecommerce_cloudera   
Tabla: conversion_1 a conversion_14 (columnas: sku (VARCHAR(50), conversion (VARCHAR(50))  
Motor: MySQL  

## Objetivo:

Calcular la conversión de venta de cada sku.  
Fórmula conversión de venta: ventas por producto / visualización producto  

La visualización de los productos se hace por medio de la siguiente página web:  
/item/id?skuID=
