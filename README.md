# PolitecStore — Análisis de datos 

Autor: LeonorYumi  
Fecha: 2026-01-27

Descripción
-----------------
Proyecto de análisis de datos para PolitecStore (tienda de tecnología). El trabajo integra múltiples fuentes (CSV, JSON, XML, SQLite y datos cloud) y se implementó principalmente con KNIME. El objetivo fue consolidar los datos, limpiarlos, obtener KPIs relevantes, segmentar clientes (RFM) y preparar visualizaciones para toma de decisiones.

Documentación
--------------------
- El workflow de KNIME con todos los pasos (carga, limpieza, consolidación, análisis y visualización).
- Datos de muestra (anonimizados) y el dataset consolidado exportado.
- Carpeta `screenshots/` con imágenes de las visualizaciones y del workflow.

Objetivo del proyecto
---------------------
Construir un pipeline reproducible que permita:
- Integrar las distintas fuentes de PolitecStore.
- Limpiar y normalizar la información.
- Consolidacion de datos
- Desplegar el dashboard 

Datos usados
------------
- ventas.csv — transacciones (id_transaccion, id_cliente, id_producto, fecha, cantidad, precio_unitario, canal)
- clientes.json — datos demográficos
- productos.xml — catálogo de productos
- inventario.sqlite — stock y movimientos históricos
- datos en la nube de mongodb

Herramientas
-----------
- KNIME Analytics Platform — workflow principal (.knwf)

Resumen del workflow (lo esencial)
---------------------------------
1. Leer fuentes con nodos File/JSON/XML/DB Reader.  
2. Normalizar nombres de columnas y tipos (fechas, numéricos).  
3. Eliminar duplicados y manejar valores faltantes (nodos Missing Value).   
4. Analizar datos 
5. Visualizacion de resultados


Despliegue
----------
- Si tienes KNIME Server: publica el workflow en KNIME WebPortal para interacción online.  

Cómo abrir el proyecto
------------------------------
1. Abrir KNIME Analytics Platform.  
2. Cargar el workflow `knime/PolitecStore_Workflow.knwf`.  
3. Revisar/editar las conexiones a bases (SQLite o credenciales cloud) en los nodos DB Connector.  
4. Ejecutar el workflow paso a paso o en bloque.  
5. Visualizar las graficas






