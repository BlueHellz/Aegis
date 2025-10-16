# 🩺 Aegis — AI Clinician App

A cross‑platform Flutter application designed as a health assistant.  
This repository currently contains the **project skeleton** — a clean, documented structure to guide development.

---


lib/ ├── main.dart # Application entry point ├── app.dart # Root widget, theme, and navigation setup ├── routes.dart # Centralized route definitions

├── core/ # Shared foundation (global utilities) │ ├── theme/ │ │ └── app_theme.dart # Global colors, typography, dark/light mode │ ├── services/ │ │ ├── api_service.dart # HTTP client for backend requests │ │ ├── websocket_service.dart # Real-time data streams │ │ └── speech_service.dart # Voice input/output (STT + TTS) │ └── utils/ │ └── formatters.dart # Helper functions (formatting, parsing, validators)

├── data/ # Data layer (models + repositories) │ ├── models/ # Data shapes (mirror backend JSON) │ │ ├── user_model.dart │ │ ├── vitals_model.dart │ │ ├── physician_model.dart │ │ ├── diagnostic_model.dart │ │ └── notification_model.dart │ └── repositories/ # Data access (API + cache) │ ├── user_repository.dart │ ├── vitals_repository.dart │ ├── physician_repository.dart │ ├── diagnostic_repository.dart │ └── notification_repository.dart

├── features/ # Each screen is self-contained │ ├── dashboard/ │ │ ├── dashboard_screen.dart # UI for dashboard │ │ ├── dashboard_controller.dart # State management │ │ └── widgets/ # Reusable dashboard widgets │ │ │ ├── conversation/ │ │ ├── conversation_screen.dart # Conversational panel (text + voice) │ │ ├── conversation_controller.dart │ │ └── widgets/ │ │ │ ├── vitals/ │ │ ├── vitals_screen.dart # Vitals input form │ │ ├── vitals_controller.dart │ │ └── widgets/ │ │ │ ├── diagnosis/ │ │ ├── diagnosis_screen.dart # Diagnostic results │ │ ├── diagnosis_controller.dart │ │ └── widgets/ │ │ │ ├── physicians/ │ │ ├── physicians_screen.dart # Physician selection │ │ ├── physicians_controller.dart │ │ └── widgets/ │ │ │ ├── oversight/ │ │ ├── oversight_screen.dart # Physician oversight notes │ │ ├── oversight_controller.dart │ │ └── widgets/ │ │ │ ├── notifications/ │ │ ├── notifications_screen.dart # Alerts and reminders │ │ ├── notifications_controller.dart │ │ └── widgets/ │ │ │ ├── history/ │ │ ├── history_screen.dart # Past sessions │ │ ├── history_controller.dart │ │ └── widgets/ │ │ │ ├── settings/ │ │ ├── settings_screen.dart # Personalization & accessibility │ │ ├── settings_controller.dart │ │ └── widgets/ │ │ │ └── session_tools/ │ ├── session_tools_screen.dart # Session management tools │ ├── session_tools_controller.dart │ └── widgets/


---

## 🧭 Design Principles

- **Feature‑first**: Each screen is isolated in its own folder with UI, controller, and widgets.
- **Separation of concerns**: Core services, data models, and repositories are centralized.
- **Scalable**: Easy to add new screens or services without breaking existing ones.
- **Consistent**: Predictable naming conventions across the app.
- **Future‑proof**: Works for MVP and production.

---

## 🚀 Next Steps

- Flesh out each placeholder file with actual code.
- Implement navigation in `routes.dart`.
- Connect repositories to real backend APIs.
- Add unit tests under `test/`.

---

## 📌 Notes

This repo currently contains **only the skeleton**.  
It’s meant as a foundation for collaborative development and to ensure clarity before implementation begins.


└── shared/ # Common reusable widgets ├── primary_button.dart # Styled button ├── loading_indicator.dart # Spinner/loading UI └── empty_state.dart # Placeholder for empty data
