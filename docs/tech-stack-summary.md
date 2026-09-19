# Tech Stack Summary — FitFlow Redesign

## Frontend — React Native (iOS + Android)

| Criterion | Flutter | React Native ✅ | Kotlin Multiplatform | Swift/SwiftUI |
|---|---|---|---|---|
| Dev speed | Fast (1 codebase) | Very fast, largest hire pool | Moderate (UI x2) | Slow (iOS only) |
| Code reuse | ~95% | ~85–90% | ~40–60% (logic) | 0% outside Apple |
| Animations | Very good | Good (New Architecture) | Excellent | Excellent (Apple only) |
| ML/CV ecosystem | Smaller | Mature ML Kit / TFLite | Smaller | Core ML only |
| Fit for FitFlow | Close 2nd | **Chosen** | UI x2 = too slow | iOS-only = ruled out |

## Backend — Node.js + Express

- Shares JS/TS with the React Native team.
- Natural fit with Firebase real-time listeners (social feed, notifications).
- Fastest to ship for a mid-sized startup.
- Paired with a small Python Cloud AI Service for model training/refresh only.

## Data & Real-time — Firebase

- **Firestore** — profiles, workout plans, nutrition journals.
- **Realtime Database** — live social feed, challenges.
- **Cloud Functions** — triggers + content moderation.
- **Cloud Messaging** — push notifications.
- **Firebase Auth** — identity, social login (targets 68% onboarding abandonment).
- Built-in offline persistence directly satisfies the offline-capability NFR.

## AI / Computer Vision

- **On-device TensorFlow Lite** — personalization inference (private + offline).
- **ML Kit** — camera-based food recognition (nutrition logger).
- **Python Cloud AI Service** — periodic model retraining & refresh.
