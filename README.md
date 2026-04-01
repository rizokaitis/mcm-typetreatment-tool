# McMaster Type Treatment Tool

A web-based tool that automates McMaster University's headline highlight type treatment according to brand guidelines.

## 🔗 Live Tool

**Use the tool online:** https://rizokaitis.github.io/mcm-typetreatment-tool/ 

No installation required — works directly in your browser.

---

## Features

- **Precise Cap Height Measurement** — Physical cap height (not bounding box) for accurate padding
- **Brand-Compliant Spacing** — 0.20× cap height (top/sides), 0.35× cap height (bottom)
- **Multi-Line Support** — Automatic highlight box positioning across line breaks
- **Live Preview** — Adjust font size (24-200px) and line height with real-time updates
- **Animated Reveal** — Fade-up text with maroon box sweep animation
- **5 Export Formats:**
  - **PNG** — Transparent background, 2× resolution
  - **SVG** — Scalable vector with embedded fonts
  - **PDF** — Print-ready document
  - **EPS (CMYK)** — Professional print with outlined paths and CMYK colors
  - **Code** — Self-contained HTML with animation

---

## For Internal Implementation

### Option 1: Use Online (Recommended)

Simply bookmark the live tool — no installation needed. All processing happens in the browser (no data is sent to servers).

### Option 2: Download & Host Internally

1. **Download the source code:**
   ```bash
   git clone https://github.com/rizokaitis/mcm-typetreatment-tool.git
   cd mcm-typetreatment-tool
   ```

2. **Host on your server:**
   - Copy `index.html` and the `Assets/` folder to your web server
   - The tool is a single HTML file with self-hosted fonts — no build process required
   - Serve via any web server (Apache, Nginx, IIS, etc.)

3. **Or open locally:**
   ```bash
   # Mac/Linux
   python3 -m http.server 8080

   # Windows
   python -m http.server 8080
   ```
   Then open: http://localhost:8080/

### Option 3: Customize the Code

The entire tool is in one file ([index.html](index.html)) with clear inline comments.

**Documentation:** See [progress.md](progress.md) for implementation details and architecture notes.

---

## Browser Support

- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari 14+

Requires modern browser with Canvas API and TextMetrics support.

---

## Technical Details

- **Zero dependencies** — Pure HTML/CSS/JavaScript
- **Self-hosted fonts** — Poppins Bold with metric overrides
- **CDN libraries** — html-to-image, jsPDF, svg2pdf.js, opentype.js (for exports only)
- **No backend** — All processing happens client-side
- **File size** — ~60KB HTML + ~140KB fonts

---

## Support

For questions or issues, please [open an issue](https://github.com/rizokaitis/mcm-typetreatment-tool/issues) or contact the design team.
