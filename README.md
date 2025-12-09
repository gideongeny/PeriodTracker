# PeriodTracker

A privacy-focused menstrual cycle tracking app built with Capacitor, Ionic React, and TypeScript for Android.

## 📱 About

PeriodTracker is a simple, secure, and user-friendly Android application designed to help users track their menstrual cycles. The app prioritizes user privacy by storing all data locally on the device - no cloud sync, no data collection, no tracking.

## ✨ Features

- **Cycle Tracking**: Track your menstrual cycle with ease
- **Privacy-First**: All data stored locally on your device
- **Multi-language Support**: Available in multiple languages including Swahili
- **Notifications**: Reminders for important cycle events
- **Modern UI**: Built with Ionic React for a beautiful, native-like experience
- **Offline-First**: Works completely offline - no internet required

## 🛠️ Tech Stack

- **Framework**: [Capacitor](https://capacitorjs.com/) 7.0
- **UI Framework**: [Ionic React](https://ionicframework.com/react) 8.4
- **Language**: TypeScript
- **Build Tool**: Vite 6.0
- **State Management**: React Hooks
- **Internationalization**: i18next
- **Testing**: Vitest

## 📋 Requirements

- Node.js 18+ and npm
- Android Studio
- JDK 17+
- Android SDK (API 23+)
- Gradle 8.7+

## 🚀 Getting Started

### Prerequisites

1. Install Node.js and npm
2. Install Android Studio
3. Set up Android SDK

### Installation

1. Clone the repository:
```bash
git clone https://github.com/gideongeny/PeriodTracker.git
cd PeriodTracker
```

2. Install dependencies:
```bash
npm install
```

3. Build the web assets:
```bash
npm run build
```

4. Sync Capacitor:
```bash
npx cap sync android
```

### Development

Run the development server:
```bash
npm run dev
```

### Building for Android

1. Open the project in Android Studio:
```bash
cd android
# Open in Android Studio
```

2. Build the app bundle:
```bash
./gradlew -p android/ bundleRelease
```

The AAB file will be generated at: `android/app/build/outputs/bundle/release/app-release.aab`

### Building APK (for testing)

```bash
./gradlew -p android/ assembleRelease
```

The APK will be at: `android/app/build/outputs/apk/release/app-release.apk`

## 📦 Project Structure

```
PeriodTracker/
├── android/              # Android native project
│   ├── app/             # Main Android app module
│   └── build.gradle     # Android build configuration
├── src/                 # Source code
│   └── utils/          # Utilities and translations
├── app/                # Built web assets (generated)
├── package.json        # Node.js dependencies
└── README.md          # This file
```

## 🌍 Internationalization

The app supports multiple languages. To add a new language:

1. Create a translation file in `src/utils/translations/`
2. Register it in your i18next configuration
3. Add Android locale resources in `android/app/src/main/res/values-{locale}/`

See [SWAHILI_SETUP.md](SWAHILI_SETUP.md) for an example.

## 🔒 Privacy

PeriodTracker is committed to user privacy:

- **No Data Collection**: We don't collect any user data
- **Local Storage Only**: All data is stored on your device
- **No Tracking**: No analytics, no tracking, no ads
- **Minimal Permissions**: Only requests necessary permissions

## 📱 App Information

- **Package Name**: `com.periodtracker.app`
- **Version**: 1.0.0
- **Min SDK**: 23 (Android 6.0)
- **Target SDK**: 35 (Android 15)
- **Compile SDK**: 35

## 🧪 Testing

Run tests:
```bash
npm test
```

Run tests in watch mode:
```bash
npm run test:watch
```

## 📝 Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm test` - Run tests
- `npm run lint` - Lint code
- `npm run fmt` - Format code with Prettier

## 📄 License

This project is open source. Please check the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📚 Documentation

- [Play Store Compliance Guide](PLAY_STORE_COMPLIANCE.md) - Guide for publishing to Google Play Store
- [Swahili Setup Guide](SWAHILI_SETUP.md) - Guide for adding Swahili language support

## 🐛 Issues

If you encounter any issues, please [open an issue](https://github.com/gideongeny/PeriodTracker/issues) on GitHub.

## 👤 Author

**PeriodTracker**

- GitHub: [@gideongeny](https://github.com/gideongeny)
- Repository: [PeriodTracker](https://github.com/gideongeny/PeriodTracker)

## 🙏 Acknowledgments

- Built with [Capacitor](https://capacitorjs.com/)
- UI components from [Ionic](https://ionicframework.com/)
- Icons from [Ionicons](https://ionic.io/ionicons)

---

**Note**: This app is designed for health and wellness purposes. It is not a medical device and should not be used as a substitute for professional medical advice.

