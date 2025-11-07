Actividad 1 – Migración de Base de Datos (Portosoft S.A.S)

Autor: Jhon Jader Benítez Valderrama
Grupo: 10
Curso: Big Data
Plataforma: Databricks
Repositorio: BigData

Descripción general

Este proyecto corresponde a la Actividad 1 del curso Big Data, cuyo propósito es aplicar los conceptos de la Unidad 1 para migrar un conjunto de datos real hacia una base de datos analítica en Databricks.

La empresa ficticia Portosoft S.A.S, dedicada al desarrollo de soluciones tecnológicas, requiere centralizar y estructurar la información de vacantes tecnológicas provenientes de archivos CSV en un entorno moderno, confiable y escalable.

Objetivo

Implementar el proceso completo de migración y modelado de datos en Databricks, desde la carga de un dataset real hasta la creación de una base de datos relacional y ejecución de consultas SQL que verifiquen la correcta estructura de la información.

Dataset utilizado

Nombre: LinkedIn Software Engineer Jobs Dataset
Autor: Andrés Ionel
Fuente: Kaggle

El dataset contiene información detallada sobre ofertas laborales del área de ingeniería de software, incluyendo título del empleo, empresa, ubicación, modalidad y habilidades requeridas.

⚙️ Proceso desarrollado

Carga del dataset:
Se importó el archivo CSV desde Kaggle al entorno de Databricks.

Creación del DataFrame:
Se generó un DataFrame de Spark (spark_df) para manejar los datos de manera distribuida.

Limpieza de columnas:
Se renombraron las columnas con espacios (por ejemplo, job level → job_level) para evitar errores en SQL.

Creación del esquema y tabla:
Se creó el esquema portosoft_db y se guardó la tabla principal utilizando el comando de escritura en Spark.

Verificación de la migración:
Se realizaron consultas SQL (SELECT, DESCRIBE TABLE, COUNT(*)) para confirmar la correcta creación de la base de datos y su estructura.

Diseño del Modelo Entidad–Relación (ERD):
Se diseñó un modelo en draw.io, estableciendo dos entidades (Company y Job) con una relación de uno a muchos (una empresa puede tener varios empleos publicados).

Documentación:
Todo el proceso se documentó en un notebook de Databricks, con celdas Markdown y SQL que describen y evidencian cada paso.

Diagrama ER

![Diagrama ER](https://raw.githubusercontent.com/jhonbenitez-source/BigData/main/Untitled.png)

Resultados

La base de datos portosoft_db se creó correctamente en Databricks.

Se almacenaron 9,380 registros válidos provenientes del dataset original.

Se ejecutaron consultas exitosas que muestran la estructura y consistencia de los datos.

Se obtuvo un modelo relacional claro para futuras integraciones con sistemas de reclutamiento o análisis de empleo.

Conclusiones

El proyecto demuestra la importancia de una migración estructurada y documentada hacia entornos de análisis modernos como Databricks.
Portosoft S.A.S ahora cuenta con una base sólida para el almacenamiento y gestión de ofertas laborales, manteniendo integridad, trazabilidad y capacidad de expansión.

Tecnologías utilizadas

Databricks

Apache Spark

PySpark

SQL

Draw.io

GitHub

Licencia: Este proyecto se realiza con fines académicos dentro del curso Big Data.