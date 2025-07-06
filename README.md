![Screenshot_1](https://github.com/user-attachments/assets/b499f2d6-3a1e-483d-8aea-d603e8a4034e)# ☄️ Pipeline de Datos de Marte con Azure Data Factory

Este repositorio contiene un pequeño proyecto de ingeniería de datos en el que armo un pipeline con **Azure Data Factory** para traer información sobre el clima en **Marte**, obtenida desde una API pública de la **NASA**.

La idea es tomar esos datos, guardarlos como archivos CSV en la nube y luego cargarlos en una base de datos SQL para que puedan ser consultados más fácilmente.

---

## ¿Qué hace este proyecto?

- Se conecta a la **API de la NASA** que publica información meteorológica recolectada por el módulo InSight en Marte.
- Guarda los datos como archivos JSON en **Azure Blob Storage**.
- Se limpian y transforman los datos con pySpark en Databricks, luego se usa notebook en pipeline
- Luego, los carga directamente en una tabla en **Azure SQL Database** (o similar) y como archivo **CSV** en ADLS.
- Todo el proceso es orquestado automáticamente con **Azure Data Factory**.

---

##  ¿Qué datos incluye?

Algunos de los datos que vas a encontrar:
- Día marciano (**sol**)
- Tiempo de medicion inicial y final
- Presión atmosférica.
- Velocidad del viento.
- Temperatura en el aire
- Promedio de velocidad del viento
- Dirección del viento en grados
- Fecha terrestre del registro.

---

##  Tecnologías utilizadas

- **Azure Data Factory** – Orquestación del pipeline.
- **Azure Blob Storage** – Almacenamiento de los archivos CSV.
- **Azure SQL Database** – Base de datos destino.
- **Azure Databricks** – Limpieza y transformación de datos.
- **API InSight Mars (NASA)** – Fuente de los datos climáticos.

---

##  ¿Para qué sirve?

Este proyecto es ideal si estás aprendiendo sobre:
- Automatización de pipelines en la nube.
- Ingesta de datos desde APIs REST.
- Limpieza y transformación de datos con Databricks.
- Procesos ETL simples en Azure.
- Integración entre servicios como ADF, Storage y SQL en un flujo funcional.

---

## Capturas

#### JSON crudo (raw) inicial ingestado desde la API de NASA Company (Problema: Doble objeto dentro del dia, no se puede ingestar directamente, da malos resultados por dia marciano)
![Screenshot_1](https://github.com/user-attachments/assets/bb48f852-47db-44ed-b4c1-09ba526f1789)

#### Conexión a API REST de la NASA, mediante APIKEY como parametro, sin activación de KEY_VAULT
![454132982-fea44fa1-fa69-4eac-bd3e-b60818c52b69](https://github.com/user-attachments/assets/df5240f2-87f3-4b4a-bbb5-b030d530db58)

#### Conexión Sink a archivo JSON raw en ADLS 
![AA](https://github.com/user-attachments/assets/b5615ecc-15b8-4c25-8922-b9ac5847691c)

### Parte de codigo PySpark para limpiar, trasnformar la ingesta de JSON raw y crear archivos parquet y CSV en ADLS limpios
![aaAa](https://github.com/user-attachments/assets/29b517c9-59c1-462d-aa6b-8c7c49d7c744)

### Copiar data de CSV a nueva tabla SQL en ASQLDB mediante dataset conectado a recurso SQL
![SDWQ](https://github.com/user-attachments/assets/f06528b3-beac-4018-9346-ae9855b128d4)

### (Final) Consulta simple para corroborar creacion, transformación de datos e ingesta desde CSV a SQL
![SQLaa](https://github.com/user-attachments/assets/d0c6686b-9a5d-4260-9837-8b6782ce6143)







