# FitFlow Redesign

A cross-platform fitness app (iOS/Android) delivering AI-personalised workout
plans, private social circles, camera-based nutrition logging and progress
dashboards — redesigned to address a personalization gap, social isolation and
onboarding friction identified through user research (see `/docs`).

## Tech Stack

- **Frontend:** React Native (iOS / Android) + on-device TensorFlow Lite + ML Kit
- **Backend:** Node.js + Express
- **Data / Real-time:** Firebase (Firestore, Realtime Database, Cloud Functions, FCM)
- **Auth:** Firebase Auth
- **AI training:** Python Cloud AI Service

## Getting Started

1. Clone the repo
2. `cd frontend && npm install && npx react-native run-ios` (or `run-android`)
3. `cd backend && npm install && npm run start:dev`
4. `cd ai-service && pip install -r requirements.txt`

## Documentation

- [Tech Stack Summary](docs/tech-stack-summary.md)
- [Comparison Matrix](docs/comparison-matrix.md)
- [Architecture Diagram](docs/architecture-diagram.png)
- [ADR-001: Technology Stack](docs/adr-001-technology-stack.md)

## Repository Settings

- `main` is protected: PR review + passing CI status checks required.
- Force-push and direct commits to `main` are disallowed.

## License

MIT — see [LICENSE](LICENSE).
