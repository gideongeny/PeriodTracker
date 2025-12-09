# Swahili Language Setup

## Translation File Created
The Swahili translation file has been created at: `src/utils/translations/sw.ts`

## How to Register Swahili in i18next

Since the source i18n configuration file was not found, you'll need to register Swahili in your i18next configuration. Typically, this is done in a file like `src/i18n.ts` or `src/utils/i18n.ts`.

### Example i18next Configuration

```typescript
import i18n from 'i18next';
import { initReactI18next } from 'react-i18next';
import en from './utils/translations/en';
import es from './utils/translations/es';
import fr from './utils/translations/fr';
import de from './utils/translations/de';
import ru from './utils/translations/ru';
import sw from './utils/translations/sw'; // Add Swahili import

i18n
  .use(initReactI18next)
  .init({
    resources: {
      en: en,
      es: es,
      fr: fr,
      de: de,
      ru: ru,
      sw: sw, // Add Swahili resource
    },
    lng: 'en', // default language
    fallbackLng: 'en',
    interpolation: {
      escapeValue: false,
    },
  });

export default i18n;
```

### Language Code
- Swahili language code: `sw`
- The translation file uses the standard i18next format

## Android Locale Support
Android locale resources have been added at:
- `android/app/src/main/res/values-sw/strings.xml`

This ensures the app name and Android system strings are properly localized for Swahili-speaking users.

## Testing
After rebuilding the app, Swahili should be available as a language option in the app settings.

