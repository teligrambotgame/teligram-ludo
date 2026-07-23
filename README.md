# Ludo King Pro - Android Studio Project Template

This is a professional Android Studio project template for a **Ludo Game** structured with **Clean Architecture** patterns, leveraging **Kotlin**, **Material Design 3**, and modern architectural recommendations.

## Project Specifications

- **Language:** Kotlin
- **Minimum SDK:** Android 8.0 (API 26 - Oreo)
- **Target SDK:** Android 14 (API 34)
- **Theme/UI Style:** Material Design 3 (MD3)
- **Package Name:** `com.ludokingpro.game`

---

## File Directory Map & Placements

To integrate these files into Android Studio, place each file at its respective path relative to your project's root folder:

### 1. Build Configurations (Root Folder)
- `build.gradle.kts` -> Put in root folder: `/`
- `settings.gradle.kts` -> Put in root folder: `/`
- `gradle/libs.versions.toml` -> Put in folder: `gradle/`

### 2. Module Build (App Level)
- `app/build.gradle.kts` -> Put in: `app/`

### 3. Application Manifest
- `app/src/main/AndroidManifest.xml` -> Put in: `app/src/main/`

### 4. Layout Assets (XML resources)
Place all layout files under `app/src/main/res/layout/`:
- `activity_splash.xml` -> `app/src/main/res/layout/activity_splash.xml`
- `activity_home.xml` -> `app/src/main/res/layout/activity_home.xml`
- `dialog_settings.xml` -> `app/src/main/res/layout/dialog_settings.xml`
- `dialog_exit.xml` -> `app/src/main/res/layout/dialog_exit.xml`

### 5. Color, String and Theme Values
Place these under `app/src/main/res/values/`:
- `colors.xml` -> `app/src/main/res/values/colors.xml`
- `strings.xml` -> `app/src/main/res/values/strings.xml`
- `themes.xml` -> `app/src/main/res/values/themes.xml`

### 6. Vector/Gradient Drawables
Place under `app/src/main/res/drawable/`:
- `bg_home_header.xml` -> `app/src/main/res/drawable/bg_home_header.xml`
- `shape_circle_green.xml` -> `app/src/main/res/drawable/shape_circle_green.xml`
- `shape_circle_blue.xml` -> `app/src/main/res/drawable/shape_circle_blue.xml`
- `shape_circle_red.xml` -> `app/src/main/res/drawable/shape_circle_red.xml`

### 7. Kotlin Source Codes
Place Kotlin files in packages corresponding to their namespaces inside `app/src/main/java/`:
- **Main Activities:** `app/src/main/java/com/ludokingpro/game/ui/`
  - `SplashActivity.kt`
  - `HomeActivity.kt`
- **Domain Models:** `app/src/main/java/com/ludokingpro/game/model/`
  - `LudoGame.kt`
- **ViewModels:** `app/src/main/java/com/ludokingpro/game/viewmodel/`
  - `HomeViewModel.kt`

---

## Clean Architecture Architecture Layers

This project structure establishes solid segregation of responsibilities:
1. **Presentation Layer (UI/View):** Activities (`SplashActivity`, `HomeActivity`) binding views via `ViewBinding` and responding to live observable data.
2. **State Management (ViewModel):** `HomeViewModel` maintains reactive, rotation-proof state configurations utilizing LiveData.
3. **Data/Domain Models:** `LudoGame` defines the pure business logic and types (Enums, Data Classes) devoid of Android framework dependencies.
