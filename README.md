# ☄️ Pipeline de Datos de Marte con Azure Data Factory

Este repositorio contiene un pequeño proyecto de ingeniería de datos en el que armo un pipeline con **Azure Data Factory** para traer información sobre el clima en **Marte**, obtenida desde una API pública de la **NASA**.

La idea es tomar esos datos, guardarlos como archivos CSV en la nube y luego cargarlos en una base de datos SQL para que puedan ser consultados más fácilmente.

---

## ¿Qué hace este proyecto?

- Se conecta a la **API de la NASA** que publica información meteorológica recolectada por el módulo InSight en Marte.
- Guarda los datos como archivos CSV en **Azure Blob Storage**.
- Luego, los carga directamente en una tabla en **Azure SQL Database** (o similar).
- Todo el proceso es orquestado automáticamente con **Azure Data Factory**.

---

##  ¿Qué datos incluye?

Algunos de los datos que vas a encontrar:
- Temperatura mínima y máxima.
- Presión atmosférica.
- Velocidad del viento.
- Día marciano (**sol**).
- Fecha terrestre del registro.

---

##  Tecnologías utilizadas

- **Azure Data Factory** – Orquestación del pipeline.
- **Azure Blob Storage** – Almacenamiento de los archivos CSV.
- **Azure SQL Database** – Base de datos destino.
- **API InSight Mars (NASA)** – Fuente de los datos climáticos.

---

##  ¿Para qué sirve?

Este proyecto es ideal si estás aprendiendo sobre:
- Automatización de pipelines en la nube.
- Ingesta de datos desde APIs REST.
- Procesos ETL simples en Azure.
- Integración entre servicios como ADF, Storage y SQL en un flujo funcional.

---