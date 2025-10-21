# Eventify - Flutter

## Description

Eventify is a mobile platform designed for event management and user interaction. It includes essential functionalities such as event administration, user connection, and social features like followers, notifications, and comments.

## Demo

[![Eventify Demo](/eventifyThumbnail.png)](https://youtu.be/iUUPOK4R6GE)

*Click on the image to watch the demo on YouTube*

## Technologies Used

- **Dart**: Programming language optimized for multi-platform applications.
- **Supabase**: Backend-as-a-service (BaaS) platform for authentication, database, and storage.
- **Firebase**: Used for push notifications and analytics.
- **Flutter Localizations**: Integrated internationalization solution.

## Project Structure

```
flutter-app/
├── lib/
│   ├── data/           # Data access layer
│   │   ├── repositories/  # Repositories for data access
│   │   └── services/      # API Services
│   ├── models/         # Data models
│   ├── providers/      # Providers for state management
│   │   └── auth_provider.dart       # Authentication provider
│   │   └── notification_provider.dart  # Notification provider
│   ├── services/       # Application services
│   │   └── auth_gate.dart           # 
│   │   └── auth_service.dart        # Authentication service
│   │   └── push_notifications.dart  # Push notifications service
│   │   └── storage_service.dart     # Storage service
│   ├── utils/          # Utilities and helpers
│   ├── view_models/    # View models (MVVM)
│   ├── views/          # Application screens
│   ├── widgets/        # Reusable components
│   ├── l10n/           # Internationalization files
│   ├── navigation.dart # Navigation system
│   ├── routes.dart     # Route definition
│   └── main.dart       # Application entry point
├── assets/            # Static resources (images, etc.)
├── fonts/             # Custom fonts
├── integration_test/  # Integration tests
├── test/             # Unit tests
└── pubspec.yaml      # Dependencies and configuration
```

## Prerequisites

- Flutter SDK (latest stable version)
- Dart SDK
- Supabase account

## Environment Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/valeraruggierotesisucv/flutter-app.git
   cd flutter-app
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Configure environment variables:
   - Create a `.env` file in the project root based on `.env.example`
   - Add the following variables:
     ```
      SUPABASE_URL=your_supabase_url
      SUPABASE_ANON_KEY=your_supabase_anon_key
      FIREBASE_API_KEY=your_firebase_key
      API_URL=your_api_url
     ```

## Running the Application

### Development

To start the application in development mode:

```bash
flutter run
```

This will compile and run the application on the connected device/emulator.

### Tests

To run the unit tests:

```bash
flutter test
```

To run the integration tests:

```bash
flutter test integration_test
```

## Deployment

### APK Generation

To generate the build:

```bash
flutter build apk --split-per-abi  # For Android (APK)
```

