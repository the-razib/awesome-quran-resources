# 🖼️ Quran Page Images

Free downloadable Quran page images (604 pages) in various formats for app development.

---

## 📸 Quran Page Images (604 Pages)

### PNG/JPG Format

#### 1. **Quran-PNG (GitHub)**
- **URL:** https://github.com/GovarJabbar/Quran-PNG
- **Stars:** 25+
- **Format:** PNG
- **Pages:** 604 pages (page_001.png to page_604.png)
- **Style:** Madina Mushaf
- **Resolution:** High quality
- **License:** Open source
- **Download:**
```bash
git clone https://github.com/GovarJabbar/Quran-PNG.git
```

#### 2. **Tarteel QUL - Mushaf Page Images**
- **URL:** https://qul.tarteel.ai/resources
- **Format:** PNG, JPG
- **Pages:** 604 pages per style
- **Available Styles:**
  - QCF V2 (King Fahd Complex)
  - Indopak 15-line
  - Uthmani Hafs
  - Warsh
  - Al-Duri
- **Resolution:** High resolution
- **License:** Open source
- **Download:** Free registration required

#### 3. **QuranHub - Quran Pages Images (GitHub)**
- **URL:** https://github.com/QuranHub/quran-pages-images
- **Stars:** 17+
- **Format:** PNG/JPG
- **Pages:** 604 pages
- **Available Styles:**
  - Hafs recitation
  - Warsh recitation
  - Tajweed color-coded
- **Special:** Includes Aya location data
- **License:** GPL-3.0
- **Download:**
```bash
git clone https://github.com/QuranHub/quran-pages-images.git
```

#### 4. **Archive.org - 604 Quran Pages PNG**
- **URL:** https://archive.org/details/604-quran-koran-book-png-written-pages-in-arabic-page-number
- **Format:** PNG
- **Pages:** 604 pages
- **Style:** Arabic Mushaf
- **Resolution:** High quality
- **License:** Public domain
- **Download:** Direct download from Archive.org

#### 5. **Archive.org - Quran Mushaf Almadinah Hafs**
- **URL:** https://archive.org/details/quran-mushaf-almadinah-hafs
- **Format:** PNG/JPG
- **Pages:** 604 pages
- **Style:** Madina Mushaf (Hafs)
- **License:** Public domain
- **Download:** Direct download from Archive.org

---

## 🎨 SVG Format (Vector)

### 6. **Quran SVG (GitHub - batoulapps)**
- **URL:** https://github.com/batoulapps/quran-svg
- **Stars:** 117+
- **Format:** SVG (Scalable Vector Graphics)
- **Pages:** 604 pages
- **Origin:** Converted from Adobe Illustrator files from King Fahd Complex
- **Advantage:** Infinite scaling without quality loss
- **License:** MIT
- **Download:**
```bash
git clone https://github.com/batoulapps/quran-svg.git
```

---

## 🌐 Quran Page Image APIs

### Live Image APIs

#### 1. **Quran Pages Images API (zeyadetman)**
- **URL:** https://quran-pages.herokuapp.com/
- **GitHub:** https://github.com/zeyadetman/quran-pages-images
- **Stars:** 6+
- **Format:** JPG via API
- **Endpoints:**
  - `GET /api/pages/:pageNumber` - Get page image URL
  - `GET /show/page/:pageNumber` - Display image
  - `GET /download/page/:pageNumber` - Download image
- **Authentication:** Required (free)
- **License:** Open source

#### 2. **Quran Images API (BetimShala)**
- **URL:** https://quran-images-api.herokuapp.com/
- **GitHub:** https://github.com/BetimShala/quran-images-api
- **Stars:** 43+
- **Format:** PNG via API
- **Endpoints:**
  - `/page/:pageNumber` - Get image path
  - `/show/page/:pageNumber` - Display image
  - `/download/page/:pageNumber` - Download image
- **License:** Open source

---

## 🎨 Vector Files (For Designers)

### Adobe Illustrator Files

#### 1. **King Fahd Complex Official Files**
- **Source:** King Fahd Glorious Quran Printing Complex
- **Format:** Adobe Illustrator (.ai)
- **Pages:** 604 pages
- **Quality:** Vector (infinite resolution)
- **Usage:** Can be converted to SVG, PNG, PDF
- **Note:** Available from official KFGQPC website

---

## 💡 Usage Tips for Developers

### Image Integration

**Flutter Example:**
```dart
// Display Quran page from API
Image.network(
  'https://quran-images-api.herokuapp.com/show/page/1',
  fit: BoxFit.contain,
)

// Display local Quran page
Image.asset(
  'assets/quran_pages/page_001.png',
  fit: BoxFit.contain,
)
```

**React/Next.js Example:**
```jsx
<img 
  src="https://quran-images-api.herokuapp.com/show/page/1"
  alt="Quran Page 1"
  style={{ width: '100%', height: 'auto' }}
/>
```

### Local Storage Strategy

**Option 1: Bundle with App**
- Include all 604 pages in app assets
- Pros: Instant access, offline-first
- Cons: Large app size (~40-100 MB)

**Option 2: Download on Demand**
- Download pages as user navigates
- Cache downloaded pages
- Pros: Smaller initial app size
- Cons: Requires internet for first view

**Option 3: Hybrid Approach**
- Bundle first Juz (30 pages)
- Download rest on demand
- Best of both worlds

### Performance Optimization

**Image Caching:**
```dart
// Flutter - Use cached_network_image
CachedNetworkImage(
  imageUrl: 'https://example.com/page_1.png',
  placeholder: (context, url) => CircularProgressIndicator(),
  errorWidget: (context, url, error) => Icon(Icons.error),
)
```

**Lazy Loading:**
- Load images only when needed
- Use pagination or infinite scroll
- Preload adjacent pages

**Image Compression:**
- Use WebP format for web
- Optimize PNG with tools like TinyPNG
- Consider progressive JPEGs

### Best Practices

1. **Choose Right Format:**
   - SVG: Best for scalability, smaller size
   - PNG: High quality, larger size
   - JPG: Good balance, lossy compression

2. **Implement Offline Mode:**
   - Cache all viewed pages
   - Allow users to download full Quran
   - Sync when online

3. **Responsive Design:**
   - Support different screen sizes
   - Implement pinch-to-zoom
   - Maintain aspect ratio

4. **Accessibility:**
   - Provide text alternative
   - Support screen readers
   - High contrast mode

---

## 🎨 Tips for Designers

### Vector Advantages

- **Infinite Scaling:** No quality loss at any size
- **Easy Editing:** Modify colors, shapes, effects
- **Smaller Files:** Vector files are often smaller
- **Print Ready:** Perfect for high-resolution printing

### Recommended Workflow

1. **Start with SVG or AI files**
2. **Edit in vector software** (Illustrator, Inkscape)
3. **Export to required formats** (PNG, JPG, WebP)
4. **Optimize for target platform** (web, mobile, print)
5. **Test on different devices**

### Color Modifications

**Tajweed Colors:**
- Use color-coded versions for learning
- Maintain consistency across pages
- Ensure sufficient contrast

**Dark Mode:**
- Invert colors for dark backgrounds
- Adjust opacity for better readability
- Test in different lighting conditions

---

**Back to [Main README](../README.md)**
