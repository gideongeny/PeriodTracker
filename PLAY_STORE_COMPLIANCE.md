# Google Play Store Compliance Checklist

## ✅ Completed Requirements

### 1. App Versioning
- ✅ **Version Code**: 1 (in `android/app/build.gradle`)
- ✅ **Version Name**: 1.0.0 (in `android/app/build.gradle` and `package.json`)
- ✅ **Package Name**: `com.periodtracker.app` (unique and consistent)

### 2. Target SDK Requirements
- ✅ **Target SDK**: 35 (Android 15) - Meets Play Store requirement
- ✅ **Compile SDK**: 35
- ✅ **Min SDK**: 23 (Android 6.0) - Supports wide range of devices

### 3. Permissions
- ✅ **Internet Permission**: Only declared permission, minimal and necessary
- ✅ **No Sensitive Permissions**: No location, camera, contacts, etc.
- ✅ **Privacy-Friendly**: App works with minimal permissions

### 4. App Bundle Format
- ✅ **AAB Format**: App builds as Android App Bundle (`.aab`)
- ✅ **Build Command**: `./gradlew -p android/ bundleRelease`

### 5. App Metadata
- ✅ **App Name**: PeriodTracker (consistent across all resources)
- ✅ **App Icon**: Custom pink-themed calendar icon
- ✅ **App Label**: Properly set in `strings.xml`

### 6. Privacy Policy
- ✅ **Privacy Policy**: Created (`PRIVACY_POLICY.txt`)
- ✅ **No Data Collection**: App stores data locally only
- ✅ **Transparent**: Clear about data handling

### 7. Content Rating
- ⚠️ **Action Required**: Submit app for content rating in Play Console
  - Category: Health & Fitness
  - Age Rating: Likely "Everyone" or "Teen" (depends on content)
  - Complete questionnaire in Play Console

### 8. App Signing
- ⚠️ **Action Required**: Sign the app bundle before upload
  - Generate signing key: `keytool -genkey -v -keystore periodtracker-release.keystore -alias periodtracker -keyalg RSA -keysize 2048 -validity 10000`
  - Configure signing in `android/app/build.gradle`:
    ```gradle
    signingConfigs {
        release {
            storeFile file('periodtracker-release.keystore')
            storePassword 'YOUR_STORE_PASSWORD'
            keyAlias 'periodtracker'
            keyPassword 'YOUR_KEY_PASSWORD'
        }
    }
    buildTypes {
        release {
            signingConfig signingConfigs.release
            // ... other config
        }
    }
    ```

### 9. App Description
- ✅ **Description**: Available in README.md
- ✅ **Short Description**: "PeriodTracker - The Period Tracker App"
- ✅ **Full Description**: Comprehensive description in README

### 10. Screenshots
- ⚠️ **Action Required**: Prepare screenshots for Play Store listing
  - Minimum: 2 screenshots (phone)
  - Recommended: 4-8 screenshots
  - Feature graphic: 1024 x 500 pixels
  - App icon: 512 x 512 pixels (already created)

### 11. Localization
- ✅ **Swahili Support**: Added Swahili translations
- ✅ **Android Locale**: Swahili locale resources added
- ✅ **Multi-language**: App supports multiple languages

### 12. Manifest Requirements
- ✅ **Exported Activities**: MainActivity properly exported
- ✅ **File Provider**: Properly configured for file sharing
- ✅ **Launch Mode**: SingleTask for proper navigation
- ✅ **Config Changes**: Handles orientation and locale changes

## 📋 Pre-Upload Checklist

Before uploading to Play Store:

1. ✅ Build signed AAB: `./gradlew -p android/ bundleRelease`
2. ⚠️ Test on multiple devices and Android versions
3. ⚠️ Complete content rating questionnaire
4. ⚠️ Prepare screenshots and graphics
5. ⚠️ Write detailed app description (short and full)
6. ⚠️ Set up app signing key
7. ⚠️ Test privacy policy link
8. ⚠️ Verify all app metadata in Play Console

## 🚀 Upload Steps

1. Go to [Google Play Console](https://play.google.com/console)
2. Create new app or select existing
3. Fill in store listing:
   - App name: PeriodTracker
   - Short description: "Track your menstrual cycle with ease"
   - Full description: (from README.md)
   - Screenshots: Upload prepared images
   - Feature graphic: Upload 1024x500 image
   - App icon: Already prepared
4. Complete content rating
5. Upload signed AAB file
6. Complete privacy policy section
7. Submit for review

## 📝 Notes

- The app is privacy-focused with local-only data storage
- No server-side data collection
- Minimal permissions (only INTERNET for potential future features)
- Target SDK 35 ensures compatibility with latest Android requirements
- Version 1.0.0 indicates a stable initial release

