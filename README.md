# EXP8_MENUS_AND_WEBVIEW

# AdaptiveListView – Menus and WebView

## 1. Project Overview

**AdaptiveListView – Menus and WebView** is an Android application developed using **Android Studio and Kotlin**. The application demonstrates the implementation of an interactive `ListView`, different types of Android menus, multiple screens, and a `WebView`.

The application allows users to select different learning topics such as **Java Programming, Python, Android Development, Data Structures, and Database**. Selecting a topic opens a separate detail page containing information about that topic.

The project is designed as an Android practical experiment for demonstrating:

* ListView
* ImageView
* Options Menu
* Context Menu
* Popup Menu
* Intent navigation
* WebView
* Multiple Activities
* XML-based UI design

---

## 2. Objectives

The main objectives of this project are:

1. To create an interactive Android application.
2. To implement a `ListView` for displaying multiple topics.
3. To use `ImageView` for displaying visual content.
4. To implement the three major types of Android menus.
5. To navigate between different Activities using `Intent`.
6. To display topic-specific information on a separate screen.
7. To implement a WebView inside the Android application.
8. To provide a simple and user-friendly interface.

---

## 3. Technologies Used

| Technology     | Purpose                         |
| -------------- | ------------------------------- |
| Android Studio | Application development         |
| Kotlin         | Programming language            |
| XML            | User interface design           |
| Android SDK    | Android application development |
| ListView       | Displaying learning topics      |
| ImageView      | Displaying images               |
| Intent         | Activity navigation             |
| Options Menu   | Application-level menu          |
| Context Menu   | Long-press menu                 |
| Popup Menu     | Anchor-based menu               |
| WebView        | Displaying web content          |

---

## 4. Application Features

### 4.1 Interactive ListView

The main screen displays a list of learning topics.

Example topics:

* Java Programming
* Python
* Android Development
* Data Structures
* Database

When the user selects a topic, the application opens a dedicated detail screen.

---

### 4.2 Topic Detail Page

Each selected topic opens a separate Activity.

The detail page contains:

* Topic title
* Topic description
* Important concepts
* Example
* Additional learning information

The user can return to the main screen using the Toolbar back button.

---

### 4.3 Options Menu

The application implements an **Options Menu** in the application toolbar.

The menu provides application-level operations such as:

* Open WebView
* About
* Exit

The Options Menu is accessed from the menu icon in the Toolbar.

---

### 4.4 Context Menu

A **Context Menu** is implemented for the ListView.

The user can long-press a topic to display contextual operations.

For example:

* Open
* Share
* Remove

The **Open** option navigates to the corresponding topic detail page.

---

### 4.5 Popup Menu

A **Popup Menu** is available through the More button.

It provides additional actions such as:

* Open WebView
* Refresh List
* Help / Information

The Popup Menu appears close to the view from which it is opened.

---

### 4.6 WebView

The application contains a WebView Activity for displaying web content inside the Android application.

The WebView demonstrates how an Android application can load and display a website without directly opening a separate browser application.

The application also provides WebView-related controls such as:

* Back
* Forward
* Refresh

---

## 5. Project Structure

```text
AdaptiveListView
│
├── app
│   │
│   └── src
│       └── main
│           │
│           ├── AndroidManifest.xml
│           │
│           ├── java
│           │   └── com.example.adaptivelistview
│           │       │
│           │       ├── MainActivity.kt
│           │       ├── TopicDetailActivity.kt
│           │       └── WebViewActivity.kt
│           │
│           └── res
│               │
│               ├── drawable
│               ├── layout
│               │   ├── activity_main.xml
│               │   ├── activity_topic_detail.xml
│               │   └── activity_webview.xml
│               │
│               ├── menu
│               │   ├── options_menu.xml
│               │   ├── context_menu.xml
│               │   └── popup_menu.xml
│               │
│               ├── values
│               │   ├── colors.xml
│               │   ├── strings.xml
│               │   └── themes.xml
│               │
│               └── mipmap
│
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

---

## 6. Main Activities

### MainActivity

`MainActivity` is the main screen of the application.

It is responsible for:

* Displaying the ListView
* Displaying topic items
* Handling normal item clicks
* Registering the Context Menu
* Opening the Popup Menu
* Handling the Options Menu
* Navigating to other Activities

---

### TopicDetailActivity

`TopicDetailActivity` displays detailed information about the selected topic.

The selected topic is passed from `MainActivity` using an `Intent`.

Example:

```kotlin
intent.putExtra("TITLE", selectedItem.title)
intent.putExtra("DESCRIPTION", selectedItem.description)
```

The detail Activity retrieves the information and displays it.

---

### WebViewActivity

`WebViewActivity` is responsible for displaying web content inside the application using Android's `WebView` component.

---

## 7. Menu Implementation

The project demonstrates three menu types.

### Options Menu

The Options Menu is displayed in the Toolbar.

```text
Options Menu
     │
     ├── Open WebView
     ├── About
     └── Exit
```

### Context Menu

The Context Menu is displayed after long-pressing a ListView item.

```text
Long Press Topic
       │
       ├── Open
       ├── Share
       └── Remove
```

### Popup Menu

The Popup Menu appears when the More button is selected.

```text
More
 │
 ├── Open WebView
 ├── Refresh List
 └── Help
```

---

## 8. WebView Implementation

The WebView is used to display web content within the application.

The project requires Internet permission in `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

A basic WebView can be initialized as:

```kotlin
val webView = findViewById<WebView>(R.id.webView)

webView.settings.javaScriptEnabled = true

webView.loadUrl("https://developer.android.com/")
```

---

## 9. How to Run the Project

### Step 1 – Open Android Studio

Open Android Studio on your computer.

### Step 2 – Open the Project

Select:

```text
Open
```

and choose the project folder.

### Step 3 – Gradle Sync

Wait for Android Studio to complete Gradle synchronization.

### Step 4 – Connect Device

Connect an Android device using USB debugging or start an Android Emulator.

### Step 5 – Run

Select the device and click:

```text
Run ▶
```

The application will be installed and launched.

---

## 10. How to Test the Application

### Test 1 – ListView

1. Launch the application.
2. View the list of topics.
3. Tap a topic.
4. Verify that the topic detail page opens.

### Test 2 – Context Menu

1. Return to the main screen.
2. Long-press a topic.
3. Verify that the Context Menu appears.
4. Select **Open**.
5. Verify that the topic detail page opens.

### Test 3 – Options Menu

1. Open the Toolbar menu.
2. Select **Open WebView**.
3. Verify that the WebView Activity opens.

### Test 4 – Popup Menu

1. Tap the **More** button.
2. Verify that the Popup Menu appears.
3. Select an available option.
4. Verify the corresponding action.

### Test 5 – WebView

1. Open WebView.
2. Verify that web content loads inside the application.
3. Test Back, Forward, and Refresh if available.

---

## 11. Expected Output

The application should provide:

```text
Main Screen
     │
     ├── Java Programming
     │       ↓
     │   Java Details
     │
     ├── Python
     │       ↓
     │   Python Details
     │
     ├── Android Development
     │       ↓
     │   Android Details
     │
     ├── Data Structures
     │       ↓
     │   Data Structures Details
     │
     └── Database
             ↓
         Database Details
```

The application should also allow the user to access:

```text
Options Menu
Context Menu
Popup Menu
WebView
```

---

## 12. Advantages

* Simple and interactive user interface.
* Demonstrates multiple Android UI components.
* Demonstrates all three major menu types.
* Provides navigation between Activities.
* Displays topic-specific information.
* Demonstrates WebView integration.
* Useful for understanding basic Android application development.

---

## 13. Conclusion

The **AdaptiveListView – Menus and WebView** application successfully demonstrates the implementation of an interactive Android application using Kotlin and XML. The application combines a ListView with topic detail pages and demonstrates **Options Menu, Context Menu, Popup Menu, Intent-based navigation, and WebView**.

This project provides practical understanding of how different Android components work together to create an interactive mobile application.
