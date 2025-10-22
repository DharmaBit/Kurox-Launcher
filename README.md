# Kurox Launcher

A modern, minimalist Android launcher with beautiful UI/UX design, built with Jetpack Compose and Kotlin.

## 🎨 Features
- ✨ **Modern UI/UX** - Beautiful black, white, and gray theme
- 🔍 **Smart Search** - Fast app search with real-time results
- 📱 **Customizable Grid** - Choose between 3-6 columns
- ⭐ **Favorites** - Quick access to your most-used apps
- 👁️ **Hide Apps** - Hide unwanted apps from your home screen
- 🎭 **Dark/Light Theme** - Automatic theme switching
- 🎬 **Smooth Animations** - Fluid transitions and micro-interactions
- 📲 **App Drawer** - Organized alphabetical list of all apps
- 📝 **App Labels Toggle** - Show or hide app names
- ** AND ALL INTRESTING FEATURES**

## 📋 Requirements

- Android Studio Ladybug | 2024.2.1 or newer
- Android SDK 35 (compileSdk)
- Minimum SDK 26 (Android 8.0)
- Target SDK 35
- Kotlin 2.1.0
- Gradle 8.7.3

## 🚀 Getting Started

### 1. Clone or Download the Project

Create a new Android Studio project and copy all the files maintaining the directory structure:

```
Kurox/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/dharmabit/kurox/
│   │       │   ├── data/
│   │       │   │   ├── model/
│   │       │   │   │   └── AppInfo.kt
│   │       │   │   └── repository/
│   │       │   │       ├── AppRepository.kt
│   │       │   │       └── PreferencesRepository.kt
│   │       │   ├── ui/
│   │       │   │   ├── components/
│   │       │   │   │   ├── AppIcon.kt
│   │       │   │   │   └── SearchBar.kt
│   │       │   │   ├── home/
│   │       │   │   │   ├── AppDrawerSheet.kt
│   │       │   │   │   ├── AppOptionsSheet.kt
│   │       │   │   │   ├── HomeScreen.kt
│   │       │   │   │   └── HomeViewModel.kt
│   │       │   │   ├── settings/
│   │       │   │   │   ├── AboutDialog.kt
│   │       │   │   │   ├── LicenseDialog.kt
│   │       │   │   │   ├── SettingsActivity.kt
│   │       │   │   │   ├── SettingsItems.kt
│   │       │   │   │   ├── SettingsScreen.kt
│   │       │   │   │   └── SettingsViewModel.kt
│   │       │   │   ├── splash/
│   │       │   │   │   └── SplashActivity.kt
│   │       │   │   └── theme/
│   │       │   │       ├── Color.kt
│   │       │   │       ├── Theme.kt
│   │       │   │       └── Type.kt
│   │       │   ├── KuroxApplication.kt
│   │       │   └── MainActivity.kt
│   │       ├── res/
│   │       │   ├── values/
│   │       │   │   ├── colors.xml
│   │       │   │   ├── strings.xml
│   │       │   │   └── themes.xml
│   │       │   └── xml/
│   │       │       ├── backup_rules.xml
│   │       │       └── data_extraction_rules.xml
│   │       └── AndroidManifest.xml
│   ├── build.gradle.kts
│   └── proguard-rules.pro
├── gradle/
│   └── libs.versions.toml
├── build.gradle.kts
├── settings.gradle.kts
└── gradle.properties
```

### 2. Sync Gradle

Open the project in Android Studio and let it sync all dependencies. This may take a few minutes.

### 3. Generate Launcher Icons

You need to create launcher icons. Use Android Studio's Image Asset tool:
1. Right-click on `res` folder → New → Image Asset
2. Select "Launcher Icons (Adaptive and Legacy)"
3. Choose your icon or create one
4. Click "Next" and "Finish"

### 4. Build and Run

1. Connect your Android device or start an emulator
2. Click the "Run" button or press Shift + F10
3. Select your device
4. The app will install and launch

## 🎨 Customization

### Changing Theme Colors

Edit `ui/theme/Color.kt` to modify the color scheme:

```kotlin
val KuroxPrimary = Color(0xFFYOURCOLOR)
val KuroxBackground = Color(0xFFYOURCOLOR)
// ... etc
```

### Adjusting Grid Layout

The grid layout is customizable through settings, but default values are in:
- `data/repository/PreferencesRepository.kt` (default: 4 columns)

### Modifying Animations

Animation configurations are in individual composables. Look for:
- `animateFloatAsState`
- `spring()` and `tween()` parameters
- `AnimatedVisibility` components

## 📦 Building Release APK

1. Open `Build` → `Generate Signed Bundle / APK`
2. Select `APK`
3. Create or select your keystore
4. Choose `release` build variant
5. Click `Finish`

The APK will be generated in `app/release/app-release.apk`

## 🔧 Tech Stack

- **Language**: Kotlin 2.1.0
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM (Model-View-ViewModel)
- **Async**: Kotlin Coroutines & Flow
- **Dependency Injection**: Manual (Application class)
- **Data Persistence**: DataStore Preferences
- **Image Loading**: Coil
- **Material Design**: Material 3
- **System UI**: Accompanist System UI Controller

## 📚 Libraries Used

| Library | Version | Purpose |
|---------|---------|---------|
| Jetpack Compose | 2024.12.01 | Modern UI toolkit |
| Material 3 | 1.3.1 | Material Design components |
| Kotlin Coroutines | 1.9.0 | Async operations |
| DataStore | 1.1.1 | Data persistence |
| Coil | 2.7.0 | Image loading |
| Accompanist | 0.36.0 | Compose utilities |
| Room | 2.6.1 | Database (prepared for future use) |

## 🐛 Known Issues

- App icons may take a moment to load on first launch
- System apps filter requires app restart to take full effect

## 🔮 Future Enhancements

- [ ] Widget support
- [ ] Gesture navigation
- [ ] Custom icon packs
- [ ] App folders
- [ ] Backup/Restore settings
- [ ] Quick settings panel
- [ ] Weather widget
- [ ] Calendar integration
- [ ] App usage statistics
- [ ] Custom gesture controls

## 🔐 Privacy Policy

Kurox Launcher respects your privacy:

- **No Data Collection**: We don't collect any personal data
- **Local Storage Only**: All settings are stored locally on your device
- **No Internet Required**: The launcher works completely offline
- **Open Source**: Code is available for review
- **No Ads**: Completely ad-free experience
- **No Tracking**: No analytics or tracking services

### Permissions Used

- `QUERY_ALL_PACKAGES`: Required to display installed apps
- `SET_WALLPAPER`: For future wallpaper features (optional)
- `VIBRATE`: For haptic feedback (optional)
- `EXPAND_STATUS_BAR`: For notification shade access (optional)

## 📄 License

```
MIT License

Copyright (c) 2025 DharmaBit

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👨‍💻 Developer

**DharmaBit**
- Package: com.dharmabit.kurox
- Version: 1.0.0
- Release Date: 2025

## 🤝 Contributing

While this is currently a personal project, contributions are welcome for:
- Bug fixes
- Performance improvements
- New features
- UI/UX enhancements
- Documentation improvements

## 📞 Support

For issues, questions, or feature requests:
- Check the documentation first
- Review existing issues
- Create a detailed bug report with:
    - Device model and Android version
    - Steps to reproduce
    - Expected vs actual behavior
    - Screenshots if applicable

## 🎯 Roadmap

### Version 1.1.0 (Planned)
- App folders functionality
- Icon pack support
- Custom gestures
- Performance optimizations

### Version 1.2.0 (Planned)
- Widget support
- Weather integration
- Calendar events
- Quick settings panel

### Version 2.0.0 (Future)
- AI-powered app suggestions
- Smart home integration
- Advanced customization
- Cloud sync

## 💡 Tips & Tricks

1. **Long press an app** to access quick options (favorite, hide, info)
2. **Use search** for fastest app access
3. **Adjust grid columns** in settings for more/less apps per row
4. **Hide system apps** to declutter your app drawer
5. **Enable animations** for smoother experience (disable if performance is slow)
6. **Use favorites** for frequently used apps

## 🏗️ Project Structure

```
com.dharmabit.kurox/
├── data/               # Data layer
│   ├── model/         # Data models
│   └── repository/    # Data repositories
├── ui/                # UI layer
│   ├── components/    # Reusable UI components
│   ├── home/          # Home screen
│   ├── settings/      # Settings screen
│   ├── splash/        # Splash screen
│   └── theme/         # Theme definitions
├── KuroxApplication   # Application class
└── MainActivity       # Main activity
```

## 🔄 Version History

### v1.0.0 (Current)
- Initial release
- Core launcher functionality
- Modern Material Design 3 UI
- App search and organization
- Customizable grid layout
- Dark/Light theme support
- Smooth animations
- Favorite apps
- Hide apps feature
- Settings panel
- About and License information

## 🙏 Acknowledgments

- **Google** for Android and Jetpack Compose
- **JetBrains** for Kotlin
- **Material Design** team for design guidelines
- **Open Source Community** for amazing libraries

## ⚠️ Disclaimer

This launcher is provided "as is" without warranty of any kind. Use at your own risk. Always keep a backup launcher installed on your device.

## 🌟 Star the Project

If you find Kurox useful, consider giving it a star! Your support helps improve the project.

---

**Made with ❤️ by DharmaBit**

For more information, visit our website (https://dharmabit.pages.dev) or follow us on social media (https://instagram.com/dharmabitdev).
