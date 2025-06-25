# meikidroid

`meikidroid` is an on-screen OCR and dictionary tool for Japanese language learners playing games on Android. It runs in the background, captures text from your screen, and displays it with dictionary definitions in a toggleable overlay, allowing for a seamless learning and gaming experience.

This app was built to solve a simple problem: looking up unknown Japanese words while playing games is cumbersome. It requires pausing, switching apps, and typing. `meikidroid` streamlines this process, making it ideal for use on Android-based gaming handhelds, but it works just as well on any modern Android phone.

## Screenshots

![Screenshot_20250601-193128](https://github.com/user-attachments/assets/3445c453-7167-417b-9a79-a13bab43f5ee)
![Screenshot_20250601-194426](https://github.com/user-attachments/assets/0a2dfc85-f8fe-4170-ba95-89ce09d19073)
![Screenshot_20250601-194938](https://github.com/user-attachments/assets/6226b8b5-53af-4e21-8d0c-f94b40d42ea1)
![Screenshot_20250601-194747](https://github.com/user-attachments/assets/97eee6f5-2d64-45d7-b533-ebd00891459c)

## How It Works

1.  The app runs a background service that continuously monitors your screen.
2.  Using Google Lens OCR technology, it extracts any Japanese text from a pre-selected region of the screen (or the full screen).
3.  When you press a configured hotkey (a gamepad button or a volume key), an overlay appears.
4.  The overlay shows the captured Japanese text and its corresponding vocabulary definitions, readings, and frequency data, retrieved from the [jpdb.io](https://jpdb.io/) API.
5.  Press the hotkey again to hide the overlay and get back to your game instantly.

## Features

-   **Real-time OCR:** Captures and recognizes Japanese text directly from your screen.
-   **jpdb.io Integration:** Provides rich dictionary lookups, including vocabulary frequency, to help you focus on learning useful words.
-   **Customizable Hotkeys:** Toggle the overlay with a variety of gamepad buttons (e.g., L3/R3, A/B/X/Y) or your device's volume keys.
-   **Selectable OCR Region:** Draw a box on the screen to limit OCR to a specific area, like a dialogue box, improving performance and accuracy.
-   **Configurable Filters:**
    -   Filter vocabulary lookups by frequency to ignore common words you already know.
    -   Automatically remove OCR lines that don't contain any Japanese characters.
-   **Adjustable Appearance:** Change the font size in the overlay for better readability.

## Requirements

This app is a tool for a specific purpose and has some important requirements to function.

#### 1. jpdb.io API Key (Mandatory)

The app **will not function** without a valid API key from [jpdb.io](https://jpdb.io/). This is used to perform all dictionary lookups. You can get your key from your account settings on the jpdb.io website. The app will prompt you to enter it in the settings.

#### 2. Android Permissions

To perform its job, the app requires several sensitive permissions. It will guide you to enable them, but here's why they are needed:

-   **Screen Capture (MediaProjection):** To see the text in your games and apps.
-   **Draw Over Other Apps:** To display the definitions overlay on top of the game.
-   **Accessibility Service:** To listen for global hotkey presses (like a gamepad button) to toggle the overlay without interfering with your game.

## Installation

You can find pre-built APK files on the [Releases page](https://github.com/rtr46/meikidroid/releases). Download the latest APK and install it on your Android device.
