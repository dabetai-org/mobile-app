# dabetai — Mobile App (Patient Hub)

<p align="center">
  <img src="https://img.shields.io/badge/React_Native-0.79-61DAFB?logo=react&logoColor=black" alt="React Native">
  <img src="https://img.shields.io/badge/Expo-53-000020?logo=expo&logoColor=white" alt="Expo">
  <img src="https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
</p>

<p align="center">
  <em>Patient mobile application for diabetes monitoring, wearable sync, and AI-powered complication risk prediction.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/mobile-app">Repository</a>
  ·
  <a href="https://github.com/dabetai-org/mobile-app/issues">Report Bug</a>
  ·
  <a href="https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf">Research Paper</a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## About dabetai

**dabetai** is a comprehensive preventive ecosystem for diabetes that predicts complications like retinopathy, nephropathy, neuropathy, and diabetic foot before they become irreversible.

This repository contains the **Mobile App** — a cross-platform application (Android/iOS) that acts as the central hub for patients to:

- Log glucose levels, food intake, medication, and physical activity
- Sync with wearables (CGMs) to extract biomarkers like heart rate and sleep quality
- View AI-powered risk predictions for diabetes complications
- Communicate with healthcare providers
- Receive early warnings for timely intervention

### Ecosystem

| Component | Repository | Stack |
|-----------|-----------|-------|
| **Mobile App** (this) | [dabetai-org/mobile-app](https://github.com/dabetai-org/mobile-app) | React Native 0.79, Expo 53, Tailwind CSS |
| **Web Portal** | [dabetai-org/web-app](https://github.com/dabetai-org/web-app) | Angular 19, Tailwind CSS |
| **Core API** | [dabetai-org/api](https://github.com/dabetai-org/api) | NestJS 11, PostgreSQL, Prisma |
| **AI Inference API** | [dabetai-org/ai-api](https://github.com/dabetai-org/ai-api) | FastAPI, Python 3.11, MongoDB |
| **AI Models** | [dabetai-org/ai-models](https://github.com/dabetai-org/ai-models) | Python, scikit-learn, XGBoost, PyTorch |
| **Landing** | [dabetai-org/landing](https://github.com/dabetai-org/landing) | Astro, Tailwind CSS |

## Features

- **AI Predictions** — Early risk alerts for diabetic complications
- **Glucose Monitoring** — Log and visualize glucose levels
- **Wearable Sync** — Connect CGMs for real-time biomarkers
- **Smart Chat** — AI assistant for diabetes inquiries
- **Health Logging** — Food, medication, and physical activity tracking
- **Doctor Connection** — Share data with healthcare providers
- **Secure Data** — JWT authentication and encryption

## Quick Start

### Prerequisites

- Node.js 18+
- Expo CLI: `npm install -g expo-cli`

### Setup

```bash
git clone https://github.com/dabetai-org/mobile-app.git
cd mobile-app
npm install
```

Create a `.env` file:

```env
API_BASE_URL="http://YOUR_IP:PORT"
```

Run the development server:

```bash
npm start
```

Scan the QR code with Expo Go or use an emulator.

## Architecture

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

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for branch naming, commit conventions, and PR workflow.

## License

This project is licensed under the GNU General Public License v3.0 — see the [LICENSE](LICENSE) file for details.

## Acknowledgments

**Authors:**
- Cardenas Cabal Fermín
- Ortiz Pérez Alejandro — alex03ortizperez@gmail.com
- Serrano Puertos Jorge Christian — christian.serrano.puertos@gmail.com

**Advisors:**
- Guarneros Nolasco Luis Rolando
- Cruz Ramos Nancy Aracely

**Academic Support:**
- Universidad Tecnológica del Centro de Veracruz
