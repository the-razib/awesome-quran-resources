# 🔤 Fonts

Quranic fonts for authentic Mushaf display and Arabic typography.

---

## Quran Fonts

### 1. **QCF (Quranic Computer Font)**
- **Types:**
  - QCF V1 (15-line Madina Mushaf)
  - QCF V2 (Updated version)
  - QCF V4 (Tajweed)
- **Download:** https://qul.tarteel.ai/docs/glyph-based
- **Features:**
  - Page-specific fonts (604 fonts for 604 pages)
  - Glyph-based rendering
  - Perfect Mushaf matching
- **Format:** TTF, WOFF
- **License:** King Fahd Complex (KFGQPC)

### 2. **Uthmani Fonts (Unicode)**
- **URL:** https://itqan.dev/en/resources/
- **Features:**
  - Unicode compliant
  - Uthmanic script
  - Cross-platform compatibility
- **Fonts Available:**
  - KFGQPC Uthmanic Script HAFS
  - Amiri Quran
  - Scheherazade New
- **License:** Open source (SIL OFL)

### 3. **Amiri Quran Font**
- **Download:** Via Google Fonts API
- **Features:**
  - High-quality Arabic typography
  - Suitable for Quran display
- **Usage:** `google_fonts: ^latest_version`
- **License:** SIL OFL

### 4. **DigitalKhatt**
- **URL:** https://itqan.dev/en/resources/
- **Features:**
  - Parametric Arabic font
  - Automatic justification
  - Curvilinear nature preservation
- **Use Case:** Advanced typesetting
- **License:** Open source

---

## Font Implementation

### Flutter Example

```dart
import 'package:google_fonts/google_fonts.dart';

Text(
  'بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ',
  style: GoogleFonts.amiriQuran(
    fontSize: 24,
    fontWeight: FontWeight.bold,
  ),
)
```

### Web CSS Example

```css
@font-face {
  font-family: 'QCF';
  src: url('path/to/qcf-font.ttf') format('truetype');
}

.quran-text {
  font-family: 'QCF', serif;
  font-size: 24px;
  direction: rtl;
}
```

---

## Font Selection Guide

**For Mushaf Layout:**
- Use QCF V2 (page-specific fonts)
- Ensures exact Madina Mushaf appearance

**For General Display:**
- Use Uthmani Unicode fonts
- Better for dynamic text
- Easier to implement

**For Web:**
- Use WOFF/WOFF2 formats
- Optimize file size
- Consider font subsetting

---

**Back to [Main README](../README.md)**
