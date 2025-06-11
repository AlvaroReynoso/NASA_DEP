# ☄️ Pipeline de Datos de Marte con Azure Data Factory

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
### Conexión a API REST de la NASA, mediante APIKEY como parametro, sin activación de KEY_VAULT
![image](https://github.com/user-attachments/assets/fea44fa1-fa69-4eac-bd3e-b60818c52b69)





