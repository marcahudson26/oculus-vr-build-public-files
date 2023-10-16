# Setup Headset and PC
- Follow oculus instuctions to set up developer account and turn on developer mode
- Install oculus app on PC and connect headset to setup Quest Link

# Setup Android Studio Flamingo 2022.2.1 Patch 2
(More Actions > SDK Manager)
- Appearance & Behaviour > System Settings > Android SDK
- Android SDK Location: C:/Users/[user]/AppData/Local/Android/Sdk
  - Click edit and install Andoird SDK and API 34
- SDK Tools (Tab)
  - ✅ Show Package Details
  - Android SDK Build-Tools 34
    - ✅ 32.0.0 - Version: 32.0.0 (previously: 30.0.3 - Version: 30.0.3)
  - NDK (Side by side)
    - ✅ 25.1.8937393
  - Android SDK Command-line tools (latest)
    - ✅ Android SDK Command-line tools (latest)
    - Android SDK Command-line tools - Version: 8.0
  - CMake
    - ✅ 3.22.1 (possibly unneeded?)
    - ✅ 3.10.2.4988404

# Setup build to android
- (In Project Settings)
  - Platform > Android > APK Packaging
    - Android Package Name: com.[company].[project]
    - Minimum SDK Version: 32 (previously: 29)
    - Target SDK Version: 32 (previously: 29)
  - Platform > Android > Build
    - Support Vulkan: true
  - Platform > Android SDK > SDKConfig
    - Location of Android SDK: C:/Users/[user]/AppData/Local/Android/Sdk
    - Location of Android NDK: C:/Users/[user]/AppData/Local/Android/Sdk/ndk/25.1.8937393
    - Location of JAVA: C:/Program Files/Android/Android Studio/jbr
    - SDK API Level: android-32 (previously: latest)
    - NDK API Level: android-29
- (On toolbar)
  - ⚙️ Settings > Preview Platform > Android Vulkan Mobile
    - (Toogle Android Icon button on toolbar to switch between Android and PC views)

# First run:
- (In Editor Preferences)
  - Level Editor - Play > Play on Device
    - Build Game Before Launch: Always
    - Pack Files for Launch: Use compressed pak files
- (Oculus Headset)
  - Plug in headset to PC, and allow access etc (assuming all is good with Oculus App on PC)
- (On toolbar)
  - 🎮 Platforms > All_Android_On_[PCNAME]
- (In Editor Preferences)
  - Once build above happens:
    - Level Editor - Play > Play on Device
      - Build Game Before Launch: Never
- Build level and lighting, so it all looks correct in Oculus when launching
  - (On toolbar)
    - Toggle Android Icon Off
    - Build > Build all levels
    - Toggle Android Icon On

# Get it running in Headset
- (On toolbar)
  - 🎮 Platforms > All_Android_On_[PCNAME]
- Run in Oculus
  - (In Headset)
    - Quit the game, or disconnect the USB from the PC
    - App Library > Search
      - In the dropdown where is says "All" select "Unknown Source"