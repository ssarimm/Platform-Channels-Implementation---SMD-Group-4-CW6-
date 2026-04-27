# Platform Specific Implementation: Battery Level (SMD-Group4-CW6)
---
## 👥 Group 4 Information
**Course:** Software for Mobile Devices (SMD)

| Name | ID |
| :--- | :--- |
| **Sarim Shah** | 22K-4299 |
| **Rayyan Zafar** | 22K-4561 |
| **Abdul Moiz Farooq** | 21K-4911 |
| **Abdul Ali Ahmed** | 21K-3379 |

---
## 📌 Project Overview
This repository contains the implementation for **Class Work 6 (CW6)** for the **Software for Mobile Devices (SMD)** course. The project demonstrates the bridge between **Flutter (Dart)** and **Native Android (Java)** using **Platform Channels**.

The application retrieves and displays the real-time battery level of the device by invoking native Android APIs that are not directly available through the standard Flutter framework.

---

## 🛠 Technical Implementation

### 1. Flutter Client (Dart)
A `MethodChannel` was established with a unique domain name: `samples.flutter.dev/battery`. We use `platform.invokeMethod('getBatteryLevel')` within an asynchronous function to request data from the host platform.

### 2. Android Host (Java)
As seen in our `MainActivity.java`, we implemented:
* A `MethodCallHandler` inside the `configureFlutterEngine` method.
* Logic to listen specifically for the `getBatteryLevel` method call.
* Usage of `BatteryManager` and `IntentFilter` APIs to fetch the current battery percentage from the Android system.

---

## 📸 Application Screenshot

### [ SCREENSHOT OF APP RUNNING ]
<img width="1080" height="2424" alt="Screenshot_20260427_123059" src="https://github.com/user-attachments/assets/401c2ca9-d019-43e3-b9f9-20730a30a3ea" />

---

## 🚀 How to Build and Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/ssarimm/Platform-Channels-Implementation---SMD-Group-4-CW6-.git](https://github.com/ssarimm/Platform-Channels-Implementation---SMD-Group-4-CW6-.git)
    ```
2.  **Get dependencies:**
    ```bash
    flutter pub get
    ```
3.  **Run the application:**
    Ensure your emulator or physical device is connected.
    ```bash
    flutter run
    ```

---

*Submitted as part of the SMD Course Work requirements - 2026*
