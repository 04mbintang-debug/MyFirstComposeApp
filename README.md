# Homework 6 – My First Compose App

## Task 3: Colour and Spacing
Colour used: Color.LightGray
Padding kept: 24.dp
What changed / what stayed the same: When changing padding from 8 dp to 48 dp, the content elements shift further away from the screen borders, creating a larger inner margin, while the overall layout structure and text contents remain identical.

## Task 4: Build Error
First error message:
AAPT: error: resource file name 'My-Picture.png' is invalid, must contain only lowercase letters, digits, and underscores.
Cause: Android resource naming rules dictate that file names in drawable must only use lowercase a-z characters, numbers, and underscores. Uppercase letters and hyphens are prohibited.
Why other errors appear: Cascading compilation errors (such as unresolved reference to R.drawable) occur because the build system fails to generate resource ID pointers when initial resource parsing fails.
Fix: Renamed the image file back to lowercase snake_case (`my_picture.png`).

## Task 5: Explore the Project
(a) MainActivity path: app/src/main/java/com/example/myfirstcomposeapp/MainActivity.kt  
Sentence: It serves as the main entry point of the Android application hosting the UI component hierarchy.
(b) Gradle file path: app/build.gradle.kts  
Sentence: It configures module-level dependencies, SDK target versions, and build settings for the app module.
(c) Launcher image line: Manifest or adaptive icon configuration referencing launcher resources.  
Sentence: It points to the default application launcher icons utilized by the system launcher.

## Task 6: Preview vs Run
When modifying text in code without re-running, the Android Studio Preview updates immediately via interactive rendering, but the compiled APK installed on the physical device or emulator remains unchanged because the app package binary hasn't been re-built and re-installed. To see updates on the device, you must trigger a new Run or Apply Changes.

## Task 7: Views vs Compose
1. Imperative UI (traditional Views) requires manually mutating UI states and calling update methods like `setText()` when data changes. Declarative UI (Compose) describes the UI state declaratively, and the framework automatically manages UI updates when states change.
2. Table of Imports:

| Composable | Package (from import) | Library layer |
|---|---|---|
| Column | androidx.compose.foundation.layout.Column | Foundation / Layout |
| Text | androidx.compose.material3.Text | Material3 (UI Library) |
| Image | androidx.compose.foundation.Image | Foundation |