# 🎵 Audio Resources

Quran recitations, audio CDNs, and related audio resources.

---

## Recitations

### 1. **Quran.com Audio CDN**
- **URL:** https://verses.quran.com/
- **Features:**
  - Multiple reciters (50+)
  - High-quality MP3
  - Word-by-word audio
  - Verse timing data
- **Format:** MP3, JSON (timing)
- **License:** Free to use

### 2. **Al Quran Cloud Audio**
- **URL:** https://cdn.alquran.cloud/
- **Features:**
  - Various reciters
  - Different audio qualities
  - Surah and Ayah level
- **Format:** MP3
- **License:** Free to use

### 3. **Tarteel AI Audio**
- **URL:** https://qul.tarteel.ai/resources
- **Features:**
  - Recitations with timestamps
  - Word-by-word segments
  - Multiple reciters
- **Format:** MP3, JSON
- **License:** Open source

### 4. **EveryAyah.com**
- **URL:** http://everyayah.com/
- **Features:**
  - Individual ayah audio files
  - Multiple reciters
  - Complete database
- **Format:** MP3
- **License:** Free to use

---

## Popular Reciters

- Sheikh Mishary Rashid Alafasy
- Sheikh Abdul Basit Abdul Samad
- Sheikh Saad Al-Ghamdi
- Sheikh Mahmoud Khalil Al-Hussary
- Sheikh Maher Al Muaiqly

---

## Audio Implementation

### Flutter Example

```dart
import 'package:audioplayers/audioplayers.dart';

final player = AudioPlayer();

Future<void> playAyah(int surah, int ayah) async {
  final url = 'https://verses.quran.com/AbdulBaset/Mujawwad/mp3/$surah\_$ayah.mp3';
  await player.play(UrlSource(url));
}
```

---

**Back to [Main README](../README.md)**
