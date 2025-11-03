# 🗺️ Geo-MVP Backend

## 📘 Descripción General

Este proyecto es el **MVP del Geocodificador**, enfocado en procesar hasta 50,000 direcciones por lote utilizando la API de **HERE Maps**.  
El backend está construido en **Node.js**, con enfoque modular, escalable y preparado para producción.

---

## 🏗️ Estructura del Proyecto

geo-mvp-backend/
│
├── 📁 src/
│   ├── 📁 config/               # Configuración general (DB, env, API Keys)
│   │   ├── db.js                # Conexión a PostgreSQL
│   │   ├── env.js               # Variables de entorno
│   │   └── hereConfig.js        # Configuración para API HERE
│   │
│   ├── 📁 controllers/          # Controladores de endpoints
│   │   ├── geocodeController.js
│   │   └── uploadController.js
│   │
│   ├── 📁 routes/               # Rutas del API
│   │   ├── geocodeRoutes.js
│   │   ├── uploadRoutes.js
│   │   └── index.js
│   │
│   ├── 📁 services/             # Lógica de negocio y servicios externos
│   │   ├── hereService.js
│   │   ├── parserService.js
│   │   ├── exportService.js
│   │   └── queueService.js
│   │
│   ├── 📁 jobs/                 # Tareas asincrónicas
│   │   └── geocodeJob.js
│   │
│   ├── 📁 models/               # Modelos de datos
│   │   └── geocodeResultModel.js
│   │
│   ├── 📁 middlewares/          # Middlewares Express
│   │   ├── errorHandler.js
│   │   ├── fileValidator.js
│   │   └── logger.js
│   │
│   ├── 📁 utils/                # Helpers y utilidades
│   │   ├── csvUtils.js
│   │   ├── timeUtils.js
│   │   └── responseUtils.js
│   │
│   ├── app.js                   # Inicialización de la app
│   └── server.js                # Configuración base de Express
│
├── 📁 scripts/                  # Scripts de despliegue/mantenimiento
│   └── init-db.sql
├── 📁 logs/                     # Logs (Winston / PM2)
├── .env.example                 # Variables de entorno de ejemplo
├── .gitignore
├── package.json
└── README.md

---

## ⚙️ Instalación y Configuración

### 1️⃣ Requisitos

- Node.js 20+  
- PostgreSQL 15+  
- Redis (para colas)  
- HERE Maps API Key  

---

### 2️⃣ Instalación

```bash
git clone https://github.com/tu-org/geo-mvp-backend.git
cd geo-mvp-backend
npm install

# GEO-MVP-BACKEND
