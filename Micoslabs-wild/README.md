# Estructura Recomendada del Proyecto — MICOS WILD

```text
MICOS_WILD/
│
├── README.md
├── .gitignore
├── docker-compose.yml
├── docs/
│   ├── arquitectura/
│   │   ├── diagramas/
│   │   ├── decisiones_tecnicas.md
│   │   └── roadmap.md
│   ├── ux_ui/
│   │   ├── wireframes/
│   │   ├── mockups/
│   │   └── design_system.md
│   ├── api/
│   │   ├── endpoints.md
│   │   └── contratos_json.md
│   └── game_design/
│       ├── economia.md
│       ├── rarezas.md
│       ├── misiones.md
│       └── progresion.md
│
├── backend/
│   │
│   ├── README.md
│   ├── requirements.txt
│   ├── .env
│   ├── alembic.ini
│   ├── Dockerfile
│   │
│   ├── app/
│   │   ├── main.py
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── security.py
│   │   │   ├── database.py
│   │   │   └── jwt.py
│   │   │
│   │   ├── api/
│   │   │   ├── routes/
│   │   │   │   ├── auth.py
│   │   │   │   ├── users.py
│   │   │   │   ├── species.py
│   │   │   │   ├── cards.py
│   │   │   │   ├── sightings.py
│   │   │   │   ├── missions.py
│   │   │   │   ├── packs.py
│   │   │   │   ├── store.py
│   │   │   │   ├── xp.py
│   │   │   │   └── analytics.py
│   │   │   │
│   │   │   └── dependencies/
│   │   │       └── auth_dependencies.py
│   │   │
│   │   ├── models/
│   │   │   ├── user.py
│   │   │   ├── species.py
│   │   │   ├── card.py
│   │   │   ├── user_card.py
│   │   │   ├── sighting.py
│   │   │   ├── mission.py
│   │   │   ├── pack.py
│   │   │   ├── transaction.py
│   │   │   └── analytics.py
│   │   │
│   │   ├── schemas/
│   │   │   ├── auth_schema.py
│   │   │   ├── user_schema.py
│   │   │   ├── species_schema.py
│   │   │   ├── card_schema.py
│   │   │   ├── sighting_schema.py
│   │   │   ├── mission_schema.py
│   │   │   └── pack_schema.py
│   │   │
│   │   ├── services/
│   │   │   ├── auth_service.py
│   │   │   ├── species_service.py
│   │   │   ├── card_service.py
│   │   │   ├── mission_service.py
│   │   │   ├── xp_service.py
│   │   │   ├── economy_service.py
│   │   │   ├── rewards_service.py
│   │   │   ├── storage_service.py
│   │   │   └── analytics_service.py
│   │   │
│   │   ├── ia/
│   │   │   ├── micodex_engine.py
│   │   │   ├── image_preprocessing.py
│   │   │   ├── vision_provider.py
│   │   │   ├── confidence_rules.py
│   │   │   └── anti_cheat.py
│   │   │
│   │   ├── repositories/
│   │   │   ├── user_repository.py
│   │   │   ├── species_repository.py
│   │   │   ├── card_repository.py
│   │   │   └── mission_repository.py
│   │   │
│   │   ├── utils/
│   │   │   ├── image_utils.py
│   │   │   ├── validators.py
│   │   │   └── helpers.py
│   │   │
│   │   └── tests/
│   │       ├── test_auth.py
│   │       ├── test_species.py
│   │       ├── test_cards.py
│   │       ├── test_missions.py
│   │       └── test_ia.py
│   │
│   ├── migrations/
│   │   └── versions/
│   │
│   ├── uploads/
│   │   ├── sightings/
│   │   └── cards/
│   │
│   └── scripts/
│       ├── seed_species.py
│       ├── import_cards.py
│       └── create_admin.py
│
├── frontend/
│   │
│   ├── README.md
│   ├── pubspec.yaml
│   ├── analysis_options.yaml
│   ├── .env
│   │
│   ├── android/
│   ├── ios/
│   ├── web/
│   │
│   ├── assets/
│   │   ├── images/
│   │   │   ├── cards/
│   │   │   ├── species/
│   │   │   ├── icons/
│   │   │   └── backgrounds/
│   │   │
│   │   ├── animations/
│   │   ├── audio/
│   │   └── fonts/
│   │
│   ├── lib/
│   │   ├── main.dart
│   │   │
│   │   ├── core/
│   │   │   ├── config/
│   │   │   │   ├── app_config.dart
│   │   │   │   └── routes.dart
│   │   │   │
│   │   │   ├── constants/
│   │   │   │   ├── colors.dart
│   │   │   │   ├── rarity.dart
│   │   │   │   └── api_constants.dart
│   │   │   │
│   │   │   ├── theme/
│   │   │   │   ├── app_theme.dart
│   │   │   │   └── text_styles.dart
│   │   │   │
│   │   │   ├── services/
│   │   │   │   ├── api_service.dart
│   │   │   │   ├── auth_service.dart
│   │   │   │   ├── storage_service.dart
│   │   │   │   └── camera_service.dart
│   │   │   │
│   │   │   └── utils/
│   │   │       ├── validators.dart
│   │   │       └── helpers.dart
│   │   │
│   │   ├── data/
│   │   │   ├── models/
│   │   │   │   ├── user_model.dart
│   │   │   │   ├── species_model.dart
│   │   │   │   ├── card_model.dart
│   │   │   │   ├── mission_model.dart
│   │   │   │   └── sighting_model.dart
│   │   │   │
│   │   │   ├── repositories/
│   │   │   │   ├── auth_repository.dart
│   │   │   │   ├── species_repository.dart
│   │   │   │   ├── card_repository.dart
│   │   │   │   └── mission_repository.dart
│   │   │   │
│   │   │   └── providers/
│   │   │       ├── auth_provider.dart
│   │   │       ├── user_provider.dart
│   │   │       ├── album_provider.dart
│   │   │       └── mission_provider.dart
│   │   │
│   │   ├── features/
│   │   │   ├── auth/
│   │   │   │   ├── screens/
│   │   │   │   │   ├── login_screen.dart
│   │   │   │   │   └── register_screen.dart
│   │   │   │   │
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── home/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── camera/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── micodex/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── album/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── cards/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── missions/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   ├── store/
│   │   │   │   ├── screens/
│   │   │   │   ├── widgets/
│   │   │   │   └── controllers/
│   │   │   │
│   │   │   └── profile/
│   │   │       ├── screens/
│   │   │       ├── widgets/
│   │   │       └── controllers/
│   │   │
│   │   └── shared/
│   │       ├── widgets/
│   │       │   ├── custom_button.dart
│   │       │   ├── xp_bar.dart
│   │       │   ├── card_tile.dart
│   │       │   └── rarity_badge.dart
│   │       │
│   │       └── animations/
│   │           ├── card_reveal.dart
│   │           └── pack_opening.dart
│   │
│   └── test/
│       ├── auth_test.dart
│       ├── home_test.dart
│       └── camera_test.dart
│
├── backoffice/
│   ├── README.md
│   ├── admin_panel/
│   ├── species_manager/
│   ├── cards_manager/
│   ├── missions_manager/
│   ├── packs_manager/
│   └── analytics_dashboard/
│
├── storage/
│   ├── species_images/
│   ├── card_assets/
│   ├── user_uploads/
│   └── seasonal_assets/
│
├── analytics/
│   ├── retention/
│   ├── funnels/
│   ├── events/
│   └── dashboards/
│
└── deployment/
    ├── nginx/
    ├── docker/
    ├── kubernetes/
    ├── github_actions/
    └── scripts/
```

---

# Tecnologías Recomendadas

## Frontend Mobile

* Flutter
* Dart
* Provider / Riverpod
* Dio (HTTP)
* GoRouter
* Camera Package
* Hive o SharedPreferences

## Backend

* FastAPI
* PostgreSQL
* SQLAlchemy
* Alembic
* JWT Authentication
* Pydantic
* Uvicorn

## IA / Vision

* Gemini Vision
* OpenAI Vision
* Roboflow
* TensorFlow Lite (futuro)

## Storage

* AWS S3
* Cloudinary
* Firebase Storage

## DevOps

* Docker
* GitHub Actions
* Nginx
* Render / Railway / AWS

---

# Arquitectura Recomendada

## Frontend

Arquitectura Feature-Based:

* Cada módulo separado.
* Fácil de escalar.
* Fácil mantenimiento.
* Reutilización de widgets.

## Backend

Arquitectura por capas:

* Routes
* Services
* Repositories
* Models
* Schemas

Esto evita lógica mezclada y permite crecer sin romper el proyecto.

---

# Orden Recomendado de Desarrollo

## Sprint 1

* Auth
* Home
* Navegación
* Base Flutter
* FastAPI inicial

## Sprint 2

* Species
* Cards
* Album
* Sistema XP

## Sprint 3

* Cámara
* Upload
* IA simulada
* Sightings

## Sprint 4

* Store
* Packs
* Misiones
* Recompensas

## Sprint 5

* Analytics
* Balance
* QA
* Deploy beta

---

# Recomendación Técnica Importante

Separar completamente:

* species → información biológica
* cards → láminas jugables
* user_cards → propiedad del jugador

Esa separación permitirá:

* temporadas
* skins
* cartas animadas
* eventos
* versiones especiales
* balance económico

sin rehacer el catálogo biológico.

---

# Estructura Ideal de Base de Datos

## Tablas principales

* users
* species
* cards
* user_cards
* sightings
* missions
* user_missions
* packs
* transactions
* rewards
* analytics_events

---

# Flujo Principal del MVP

```text
Usuario abre app
    ↓
Toma foto
    ↓
Se envía al backend
    ↓
MicoDex analiza
    ↓
Backend valida
    ↓
Se desbloquea carta
    ↓
Usuario gana XP
    ↓
Actualiza álbum
    ↓
Nueva misión disponible
```

---

# Objetivo del MVP

El MVP debe validar:

* Retención
* Engagement
* Coleccionismo
* Recompensa por exploración
* Uso repetido de cámara
* Interacción con misiones
* Interés por BioSobres

La prioridad NO es monetizar primero.
La prioridad es validar el loop jugable.
