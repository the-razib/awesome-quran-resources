# 🌐 Quran APIs

Free REST APIs for accessing Quran text, translations, audio, and related data.

---

## Free REST APIs

### 1. **Quran.com API**
- **URL:** https://api.quran.com
- **Documentation:** https://quran.com/en/developers
- **Features:**
  - 90+ translations
  - Audio recitations with timestamps
  - Word-by-word data
  - Tafsir (commentary)
  - Verse timing data
- **Language Support:** 40+ languages
- **Rate Limit:** None
- **License:** Open source
- **GitHub:** https://github.com/quran

### 2. **Al Quran Cloud API**
- **URL:** https://alquran.cloud/api
- **Documentation:** https://alquran.cloud/api
- **Features:**
  - Ayah, Surah, Juz endpoints
  - Multiple reciters audio
  - Translations in 50+ languages
  - Tajweed data
  - Search functionality
- **Rate Limit:** None
- **License:** Free to use
- **Response Format:** JSON

### 3. **Quran API (Vercel)**
- **URL:** https://quranapi.pages.dev
- **Features:**
  - No rate limit
  - No authentication required
  - Verses, chapters, and audio
  - Tafsir for each verse
- **GitHub:** Open source
- **License:** MIT

### 4. **Al-Quran API (Multilingual)**
- **URL:** https://alquran-api.pages.dev
- **Features:**
  - 12+ languages supported
  - All 114 surahs
  - 6,236 verses indexed
  - Translations included
  - Edge Runtime for fast response
- **Rate Limit:** None
- **License:** Free & Open Source

### 5. **Tarteel AI - Quranic Universal Library (QUL)**
- **URL:** https://qul.tarteel.ai
- **Documentation:** https://qul.tarteel.ai/docs
- **Features:**
  - Quran text and translations
  - Mushaf layouts (multiple styles)
  - Recitations with word-by-word timestamps
  - Tafsir database
  - Mutashabihat lists
  - Auditing tools
- **License:** Open source
- **GitHub:** https://github.com/TarteelAI/quranic-universal-library
- **Special:** Largest library of Quranic content

### 6. **Quran-api (90+ Languages)**
- **URL:** https://api.quran.com
- **Features:**
  - 90+ different languages
  - 400+ translations
  - Audio recitations
- **Documentation:** https://github.com/quran/quran-api
- **License:** Open source

### 7. **Islamic API Collection**
- **URL:** https://github.com/Mohamed20a/Islamic-API
- **Features:**
  - Prayer times API
  - Quran API
  - Quran audio API
  - Tafsir API
  - Hadith API
  - Azkar (Dhikr) API
  - Radio API (18 reciters)
- **Language:** Arabic & English
- **License:** Open source

---

## API Usage Tips

### Best Practices

1. **Caching:** Cache responses to reduce API calls
2. **Error Handling:** Implement proper error handling
3. **Rate Limiting:** Respect rate limits (even if none specified)
4. **Attribution:** Credit the API provider in your app
5. **Offline Mode:** Store data locally for offline access

### Example Integration (Flutter)

```dart
import 'package:http/http.dart' as http;
import 'dart:convert';

Future<Map<String, dynamic>> fetchSurah(int surahNumber) async {
  final response = await http.get(
    Uri.parse('https://api.alquran.cloud/v1/surah/$surahNumber')
  );
  
  if (response.statusCode == 200) {
    return json.decode(response.body);
  } else {
    throw Exception('Failed to load surah');
  }
}
```

---

**Back to [Main README](../README.md)**
