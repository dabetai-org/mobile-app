# dabetai — App Móvil (Paciente)

<p align="center">
  <img src="https://img.shields.io/badge/React_Native-0.79-61DAFB?logo=react&logoColor=black" alt="React Native">
  <img src="https://img.shields.io/badge/Expo-53-000020?logo=expo&logoColor=white" alt="Expo">
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
</p>

<p align="center">
  <em>Aplicación móvil para pacientes con diabetes, con monitoreo de glucosa, sincronización con wearables y predicción de riesgos de complicaciones mediante IA.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/mobile-app">Repositorio</a>
  ·
  <a href="https://github.com/dabetai-org/mobile-app/issues">Reportar Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Artículo de Investigación</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## Acerca de dabetai

**dabetai** es un ecosistema preventivo integral para la diabetes que predice complicaciones como retinopatía, nefropatía, neuropatía y pie diabético antes de que sean irreversibles.

Este repositorio contiene la **App Móvil** — una aplicación multiplataforma (Android/iOS) que funciona como centro principal para que los pacientes puedan:

- Registrar niveles de glucosa, comidas, medicación y actividad física
- Sincronizar con wearables (MCG) para obtener biomarcadores como ritmo cardíaco y calidad del sueño
- Ver predicciones de riesgo de complicaciones generadas por IA
- Comunicarse con profesionales de la salud
- Recibir alertas tempranas para una intervención oportuna

### Ecosistema

| Componente | Repositorio | Stack |
|-----------|-----------|-------|
| **App Móvil** (este) | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Portal Web** | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **API de IA** | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **Modelos IA** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Funcionalidades

- **Predicciones IA** — Alertas tempranas de riesgo de complicaciones diabéticas
- **Monitoreo de Glucosa** — Registro y visualización de niveles
- **Sincronización Wearable** — Conexión con MCG para biomarcadores en tiempo real
- **Chat Inteligente** — Asistente IA para consultas sobre diabetes
- **Registro de Salud** — Comidas, medicación y actividad física
- **Conexión con Médicos** — Compartir datos con profesionales de la salud
- **Datos Seguros** — Autenticación JWT y encriptación

## Inicio rápido

### Prerrequisitos

- Node.js 18+
- Expo CLI: `npm install -g expo-cli`

### Instalación

```bash
git clone https://github.com/dabetai-org/mobile-app.git
cd mobile-app
npm install
```

Crea un archivo `.env`:

```env
API_BASE_URL="http://TU_IP:PUERTO"
```

Ejecuta el servidor de desarrollo:

```bash
npm start
```

Escanea el código QR con Expo Go o usa un emulador.

## Arquitectura

```
┌───────────────────────────────────────────────┐
│           Mobile App (React Native)            │
│  ┌─────────┐ ┌──────────┐ ┌──────────────┐   │
│  │ Health  │ │   AI     │ │  Wearable    │   │
│  │ Logger  │ │ Insights │ │    Sync      │   │
│  └────┬────┘ └────┬─────┘ └──────┬───────┘   │
│       │           │              │            │
│  ┌────▼───────────▼──────────────▼───────┐    │
│  │         HTTP Services (Axios)         │    │
│  └────────────────┬──────────────────────┘    │
└───────────────────┼──────────────────────────┘
                    │ JWT Auth
         ┌──────────┴──────────┐
         ▼                     ▼
┌──────────────┐     ┌──────────────┐
│  Core API    │     │  AI API      │
│  (NestJS)    │     │  (FastAPI)   │
└──────────────┘     └──────────────┘
```

## Contribuciones

Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para nuestras convenciones de ramas, commits y flujo de PRs.

## Licencia

Este proyecto está licenciado bajo GNU General Public License v3.0 — consulta el archivo [LICENSE](LICENSE) para más detalles.

## Reconocimientos

**Autores:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Asesores:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Apoyo Académico:**
- Universidad Tecnológica del Centro de Veracruz
