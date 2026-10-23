# 🚀 API de Predicción de Ventas y MLOps

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

> **Proyecto Final - Ingeniería para IA**  
> **Autor:** Paul Damian Sarro  
> **Universidad:** Universidad María Auxiliadora (UMA)

---

## 📝 Descripción del Proyecto

Este proyecto consiste en una API RESTful desarrollada con **FastAPI** que expone un modelo de Machine Learning (Regresión Lineal) para predecir ventas diarias. Además, el sistema está diseñado bajo prácticas modernas de **MLOps**, incluyendo despliegue Blue/Green, seguridad mediante API Keys, auditoría de eventos y contenerización con Docker.

## ✨ Características Principales

- 🧠 **Predicción de Ventas:** Modelo de Scikit-Learn entrenado para estimar ventas según el día.
- 🔄 **Despliegue Blue/Green:** Capacidad de alternar en caliente entre dos versiones del modelo (`BLUE` y `GREEN`) sin detener el servicio.
- 🔒 **Seguridad:** Endpoints protegidos mediante validación de `API Key`.
- 📝 **Auditoría y Logs:** Registro detallado de accesos, predicciones, latencias y cambios de modelo en archivos `.log`.
- 💬 **Módulo RAG (Consulta):** Endpoint que genera respuestas en lenguaje natural consultando una base de datos CSV de ventas.
- 🐳 **Dockerizado:** Listo para desplegarse en cualquier entorno mediante contenedores.

---

## 📂 Estructura del Proyecto

```text
proyecto_final/
│
├── app/                  # Código fuente de la aplicación
│   ├── api.py            # Endpoints principales y lógica de FastAPI
│   ├── audit.py          # Configuración del sistema de auditoría
│   ├── rag.py            # Lógica de consulta de datos (CSV)
│   └── security.py       # Validación de API Key
│
├── data/                 # Datos de entrenamiento (ventas.csv)
├── logs/                 # Archivos de registro (audit, deployment, predicciones)
├── models/               # Modelos entrenados (.pkl)
├── src/                  # Scripts de Machine Learning
│   ├── predict.py        # Script de prueba de predicción
│   └── train.py          # Script de entrenamiento del modelo
│
├── tests/                # Pruebas unitarias (pytest)
├── Dockerfile            # Configuración para contenerización
├── requirements.txt      # Dependencias del proyecto
└── README.md             # Documentación del proyecto