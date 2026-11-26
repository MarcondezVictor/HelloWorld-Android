# Hello World – Android

**Mobile Systems · Project 1**
Victor Lopes · Erasmus student at Bialystok University of Technology (Politechnika Białostocka)

A first Android application built with **Kotlin** and **Jetpack Compose**, created to set up the Android development environment and run an app on an emulator / physical device.

## What it does

Displays a personalised "Hello World" screen with a dark background:

- **Hello World!** – main title
- **Cześć! I'm Victor 👋** – personalised greeting
- **Erasmus @ Politechnika Białostocka** – subtitle

## Project structure

| File | Purpose |
|------|---------|
| `app/src/main/java/com/example/helloworld/MainActivity.kt` | Entry point of the app – `onCreate()` sets the UI with `setContent { }` |
| `app/src/main/AndroidManifest.xml` | Registers `MainActivity` as the launcher activity (`MAIN` / `LAUNCHER`) |
| `app/build.gradle.kts` | Module configuration – SDK versions and dependencies (Compose, Material 3) |
| `gradle/libs.versions.toml` | Central version catalog for libraries |

## How it works

- `MainActivity` extends `ComponentActivity` and is the first screen launched.
- `setContent { }` replaces XML layouts with a **Composable** UI.
- `HelloScreen(name)` is a `@Composable` function that uses a `Column` to stack three `Text` elements, centered vertically and horizontally.
- `Modifier` handles size (`fillMaxSize`), background colour and padding.
- `@Preview` renders the screen inside Android Studio without running the emulator.

## How to run

1. Clone the repository:
   ```bash
   git clone https://github.com/MarcondezVictor/HelloWorld-Android.git
   ```
2. Open the folder in **Android Studio** and wait for the Gradle sync.
3. Select an emulator or a connected device and press **Run ▶**.

## Tech stack

- Kotlin
- Jetpack Compose + Material 3
- Android Studio · Gradle (Kotlin DSL)
