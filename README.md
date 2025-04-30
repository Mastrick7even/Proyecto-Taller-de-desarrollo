# Sistema de Alerta Temprana - Deserción Estudiantil UBB

## ✨ Descripción

Este proyecto tiene como objetivo desarrollar un sistema inteligente de alerta temprana para **prevenir la deserción de estudiantes de primer año** en la Universidad del Bío-Bío. Utiliza modelos de **Machine Learning** para identificar estudiantes en riesgo y proporciona herramientas visuales (dashboards) y reportes para apoyar la toma de decisiones de **tutores y encargados de carrera** del Programa de Tutores.

## 🏗️ Arquitectura del Proyecto

El sistema sigue una arquitectura de aplicación web moderna, separando la lógica del backend, el frontend y la base de datos, orquestado mediante Docker:

* **Frontend (Dashboard):** Interfaz web interactiva desarrollada con **Plotly Dash** (o **Streamlit**) para visualización de datos y alertas.
* **Backend (API):** API RESTful construida con **FastAPI (Python)** para manejar la lógica de negocio, predicciones y comunicación con la base de datos.
* **Base de Datos:** **PostgreSQL** para almacenar datos académicos, de seguimiento y resultados de las predicciones.
* **Machine Learning:** Modelos predictivos desarrollados con **Scikit-learn** y **Pandas** para el análisis y procesamiento de datos.
* **Autenticación:** *(Por definir o implementar según necesidad futura - ej. tokens simples)*
* **Despliegue:** Contenerizado con **Docker** y orquestado con **Docker Compose**.

## 💻 Tecnologías Utilizadas

* **Lenguaje:** Python 3.10+
* **Framework Backend:** FastAPI
* **Framework Frontend/Dashboard:** Plotly Dash (o Streamlit)
* **Base de Datos:** PostgreSQL 15
* **Machine Learning:** Scikit-learn, Pandas, NumPy
* **Contenerización:** Docker, Docker Compose
* **Servidor ASGI:** Uvicorn

## 🚀 Instalación y Uso (Desarrollo Local)

1.  **Clonar el repositorio:**
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd <NOMBRE_CARPETA_PROYECTO>
    ```
2.  **Configurar Variables de Entorno:**
    * Crea un archivo `.env` en la raíz del proyecto copiando el archivo `.env.example` (si existe) o basándote en el ejemplo proporcionado.
    * Ajusta las credenciales de la base de datos (`POSTGRES_USER`, `POSTGRES_PASSWORD`, `POSTGRES_DB`) y cualquier otra configuración necesaria en el archivo `.env`.
3.  **Construir e Iniciar los Contenedores:**
    * Asegúrate de tener Docker y Docker Compose instalados y Docker Desktop ejecutándose.
    * Ejecuta el comando:
        ```bash
        docker compose up --build
        ```
4.  **Acceder a la Aplicación:**
    * API Docs (Swagger UI): Abre tu navegador en `http://localhost:8000/docs`
    * Frontend/Dashboard: Accede a `http://localhost:8000` (o el puerto que corresponda si usas Dash/Streamlit en un puerto diferente configurado en docker-compose).
