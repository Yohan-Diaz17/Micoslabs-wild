# 🐾 MICOS WILD

> App móvil de colección de biodiversidad real asistida por IA.
> Inspirada en el concepto de una Pokédex, pero enfocada en fauna y flora reales.

---

# 🌎 ¿Qué es MICOS WILD?

MICOS WILD es una aplicación móvil multiplataforma desarrollada con Flutter + FastAPI que permite a los usuarios:

* 📸 Fotografiar especies reales.
* 🧠 Identificarlas mediante IA (MicoDex).
* 🃏 Desbloquear láminas coleccionables.
* ⭐ Ganar XP y subir de nivel.
* 🌱 Obtener Semillas y recompensas.
* 🎯 Completar misiones.
* 📚 Construir un álbum de biodiversidad.

El objetivo del proyecto es transformar la exploración de biodiversidad en una experiencia jugable, educativa y escalable.

---

# 🎮 Filosofía del Producto

MICOS WILD NO busca ser inicialmente una plataforma infinita.

La prioridad es construir una:

## "Vertical jugable"

Es decir:

```text
Foto → IA → Lámina → XP → Recompensa → Nueva exploración
```

Si ese loop funciona y genera retención:

✅ El producto existe.

---

# 🚀 Objetivo del MVP

El MVP debe permitir:

* Login y registro.
* Captura o subida de imágenes.
* Identificación asistida por IA.
* Desbloqueo de láminas.
* Álbum coleccionable.
* Sistema de XP y niveles.
* Misiones básicas.
* Store con BioSobres.
* Analytics y métricas.

---

# 🧱 Stack Tecnológico

## 📱 Frontend

| Tecnología          | Uso                        |
| ------------------- | -------------------------- |
| Flutter             | Desarrollo multiplataforma |
| Dart                | Lenguaje principal         |
| Provider / Riverpod | Manejo de estado           |
| Dio                 | Consumo de API             |
| GoRouter            | Navegación                 |
| Camera Package      | Captura de imágenes        |

---

## ⚙️ Backend

| Tecnología | Uso                     |
| ---------- | ----------------------- |
| FastAPI    | API REST                |
| PostgreSQL | Base de datos principal |
| SQLAlchemy | ORM                     |
| Alembic    | Migraciones             |
| JWT        | Autenticación           |
| Pydantic   | Validaciones            |

---

## 🧠 IA / Vision

Posibles proveedores:

* Gemini Vision
* OpenAI Vision
* Roboflow
* TensorFlow Lite (futuro)

---

## ☁️ Storage

* AWS S3
* Cloudinary
* Firebase Storage

---

# 🏗️ Arquitectura General

```text
App Flutter
    ↓
FastAPI Gateway
    ↓
Servicios de Juego
    ↓
MicoDex (IA)
    ↓
PostgreSQL + Storage
```

---

# 📂 Estructura del Proyecto

```text
MICOS_WILD/
│
├── backend/
├── frontend/
├── docs/
├── analytics/
├── storage/
├── deployment/
└── backoffice/
```

---

# 🧬 Modelo de Dominio

## Entidades principales

### User

Información del jugador.

### Species

Información biológica real.

### Card

Representación coleccionable.

### UserCard

Propiedad de cartas del usuario.

### Sighting

Capturas realizadas por el usuario.

### Mission

Misiones y objetivos.

### Pack

BioSobres.

### Transaction

Economía y auditoría.

---

# 🧠 MicoDex — Sistema IA

Pipeline de procesamiento:

```text
Captura
   ↓
Preproceso
   ↓
Vision IA
   ↓
Validación
   ↓
Recompensa
```

---

# 🎯 Reglas de Confianza

| Confianza | Resultado           |
| --------- | ------------------- |
| >= 75%    | Desbloqueo completo |
| 50% - 74% | XP parcial          |
| < 50%     | Reintento guiado    |

---

# 🛡️ Anti-Abuso

* Hash perceptual anti-duplicado.
* Límites diarios de capturas.
* Validación de rarezas.
* Recompensa superior para captura en vivo.

---

# 🎮 Economía del Juego

## Fuentes de láminas

* Fotos reales.
* BioSobres.
* Misiones.
* Eventos.

## Recompensas

* XP.
* Semillas.
* Cartas.
* Desbloqueos.

## Filosofía

```text
NO PAY TO WIN
```

Explorar debe recompensar mejor que comprar.

---

# 📱 Pantallas del MVP

## Home

* Nivel
* XP
* Misión activa
* Acceso rápido a cámara

## Cámara

* Captura
* Subida
* IA

## MicoDex

* Resultado IA
* Confianza
* Datos especie

## Álbum

* Colección
* Progreso
* Cartas bloqueadas

## Store

* BioSobres
* Semillas
* Packs

---

# 📈 KPIs del MVP

## Objetivos iniciales

| KPI                       | Objetivo |
| ------------------------- | -------- |
| D1 Retention              | >= 25%   |
| Capturas promedio         | >= 2     |
| Primera misión completada | >= 60%   |
| Tiempo primera lámina     | < 3 min  |

---

# 🛣️ Roadmap

## Fase 0 — Product Sprint

* GDD
* Dataset inicial
* Diseño visual

## Fase 1 — Vertical Slice

* Login
* Home
* Álbum
* XP

## Fase 2 — Captura + IA

* Cámara
* Upload
* IA simulada

## Fase 3 — Misiones + Store

* Packs
* Semillas
* Rewards

## Fase 4 — Beta Cerrada

* QA
* Analytics
* Balance
* APK/TestFlight

---

# 🧪 Estado Actual

## En desarrollo

Actualmente se está construyendo:

* Estructura base del proyecto.
* Arquitectura backend.
* Aplicación Flutter.
* Sistema de autenticación.
* Modelos de dominio.

---

# ⚡ Instalación Local

## Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

---

## Frontend

```bash
cd frontend
flutter pub get
flutter run
```

---

# 🔐 Variables de Entorno

## Backend

```env
DATABASE_URL=
SECRET_KEY=
JWT_ALGORITHM=
VISION_API_KEY=
```

---

# 🧩 Principios Técnicos

## Separación crítica

```text
Species   → dato biológico
Card      → lámina jugable
UserCard  → propiedad del jugador
```

Esto permite:

* temporadas
* skins
* eventos
* rarezas
* cartas animadas
* balance económico

sin rehacer el catálogo.

---

# 📊 Analítica

Se medirán:

* Retención.
* Tiempo de sesión.
* Capturas.
* Uso de cámara.
* Misiones completadas.
* Apertura de sobres.
* Engagement.

---

# 🧠 Visión del Proyecto

MICOS WILD busca convertirse en:

* Una plataforma de educación ambiental.
* Un sistema jugable de biodiversidad.
* Un ecosistema coleccionable.
* Un producto escalable para educación y conservación.

---

# 👨‍💻 Equipo Base Recomendado

* Product Owner
* Flutter Developer
* Backend Developer
* UX/UI Designer
* QA Tester
* IA / Vision Engineer

---

# 📄 Licencia

Proyecto privado.

Todos los derechos reservados © Micos Labs.

---

# 🐒 Micos Labs

Construyendo experiencias jugables basadas en biodiversidad real.
