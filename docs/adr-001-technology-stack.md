# ADR-001: Adopt React Native + Node/Express + Firebase + On-device TensorFlow Lite

**Status:** Accepted

**Context**
User research found a personalization gap, social isolation, tracking friction
and low motivation, with 68% onboarding abandonment. Functional requirements
call for an AI workout engine, private social circles, camera-based nutrition
logging and progress dashboards; non-functional requirements call for
performance, offline capability, accessibility, and GDPR/CCPA-aligned security
— all under a mid-sized startup's cost and time-to-market pressure.

**Decision**
Use React Native for the iOS/Android client with on-device TensorFlow Lite and
ML Kit; Node.js/Express for the core API; Firebase (Firestore, Realtime
Database, Cloud Functions, Cloud Messaging, Auth) as the managed
data/real-time/identity platform; a small Python Cloud AI Service for model
training and refresh.

**Consequences**
- Fast cross-platform shipping; large JS hire pool.
- Managed Firebase reduces ops cost; offline persistence built in.
- On-device inference minimizes personal data transmission (GDPR/CCPA).
- Trade-offs: dependency-fragmentation risk in React Native native modules;
  Firebase vendor tie-in for data layer.
