# 🔌 Smart Plug Taskbar Widget (Windhawk Mod)

This project is a custom mod for **Windhawk** that adds a convenient control button for your smart plug (Tuya/Smart Life) directly to the Windows taskbar. 

Instead of reaching for your phone or opening dedicated apps, you can turn your devices (e.g., lights, heaters, or routers) on and off with a single mouse click.

## ✨ Key Features
* **Native Integration:** The icon becomes a seamless part of the Windows taskbar.
* **Gamer Friendly:** The widget automatically hides when you launch a game or video in full-screen mode (doesn't overlap the UI).
* **Auto-Installation:** The mod automatically downloads the necessary `.exe` file and icons on its first run — no manual archive extraction needed!
* **Easy Configuration:** All smart plug details (Device ID, IP, Local Key) are entered through the standard Windhawk settings menu.
* **Hybrid Architecture:** Fast and lightweight UI built with `C++ (Win32 API)` combined with a reliable backend written in `Python (TinyTuya)`.

## ⚙️ How It Works
The mod creates a transparent child window (`WS_CHILD`) attached to the taskbar (`Shell_TrayWnd`). Upon clicking, it calls a hidden compiled Python script (`plug_tool.exe`) that sends a command to the plug locally (via Wi-Fi), ensuring maximum speed without cloud server delays.
