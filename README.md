# Adaptive Learning – Menus and WebView

This Android Studio project demonstrates an interactive Android application containing:

## Three Types of Menus

1. **Options Menu** – open the three-dot menu in the app bar.
   - Open WebView
   - About
   - Exit

2. **Context Menu** – long-press any learning topic.
   - Open Topic
   - Share Topic
   - Remove Topic

3. **Popup Menu** – tap the **More** button.
   - Open WebView
   - Refresh List
   - How to use menus

## WebView

The WebView opens the Android Developers website inside the application. It also provides Back, Forward and Refresh actions.

## How to Run

1. Extract/open this project in Android Studio.
2. Allow Gradle Sync to complete.
3. Connect an Android device or start an emulator.
4. Click **Run**.
5. Test all three menus.
6. Long-press a topic to test the Context Menu.
7. Open WebView from either the Options Menu or Popup Menu.

Internet permission is already included in `AndroidManifest.xml`.

## Experiment Title

**Implement Menus and WebView in an Android Application**

## Expected Result

The application displays a learning-topic ListView, supports Options Menu, Context Menu and Popup Menu interactions, and loads a website using Android WebView.


## Build fix
The project uses `Theme.AppCompat.Light.NoActionBar` with an AppCompat Toolbar. This avoids the missing `Theme.MaterialComponents.DayNight.NoActionBar` resource error and keeps the Options Menu visible in the toolbar.
