# 🎵 VTT Editor Pro v3.0

🚀 **[Try it online → https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v3.0.html](https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v3.0.html)**

A modern, lightweight, and powerful WebVTT subtitle editor that runs entirely in your browser. No installation, no signup, no cloud dependencies – just one HTML file.

**Clean starting point:**
![VTT Editor Pro v3.0 - Empty State](screenshot-empty.png)

**In action with live preview:**
![VTT Editor Pro v3.0 - Active Editing](screenshot-active.png)

---

## ✨ Features

### 🎨 **Modern Interface**
- Clean, themed UI with 5 color themes
- Color-coded regions for easy organization
- Real-time waveform visualization
- Responsive timeline with zoom controls
- Minimap for global timeline overview
- Enhanced visual resize handles with real-time tooltips

### ⚡ **Powerful Editing**
- **Drag & Drop**: Move and resize regions directly on the timeline
- **Visual Resize Handles**: See exact timestamps while resizing regions
- **Snap-to-Grid**: Align regions precisely with configurable intervals (10ms to 1s)
- **Split & Merge**: Divide cues or combine consecutive ones
- **Shift All Timings**: Offset all cues by ±X seconds
- **Batch Text Editing**: Transform multiple cues at once with Find & Replace
- **Anti-overlap Enforcement**: Optional feature to prevent subtitle collisions
- **Live Preview**: Scrolling lyrics display synchronized with playback
- **Auto-save**: Your work is saved every 5 seconds (localStorage)

### 🎯 **Workflow Optimized**
- Import MP3/audio files directly
- Import/Export VTT, SRT, ASS, SBV, DFXP, JSON formats
- Real-time cue search and filtering
- Keyboard shortcuts for rapid editing
- Precise timestamp control with snap-to-grid
- Visual waveform for accurate timing
- Undo/Redo with 20-step history

### 🚀 **Technical Highlights**
- **6900+ lines** of vanilla JavaScript – no frameworks
- **~200 MB RAM** usage
- **Offline-first**: Works without internet connection
- **Single file**: Just download and open in your browser
- Zero external dependencies (except WaveSurfer.js CDN)
- **Support for 1000+ cues and markers without lag**

---

## 🆕 What's New in v3.0

### ✂️ Édition Avancée

#### Split Cue - Diviser un cue
Divide a cue into two parts at the current cursor position.

**Features:**
- Place the playhead where you want to split
- Creates two new cues from one
- Preserves original color and styling
- Validates minimum duration (0.1s per cue)

#### Merge Cues - Fusionner des cues
Combine two consecutive cues into a single one.

**Features:**
- Select the first cue, then merge with the next
- Text is combined with a line break
- Warning if gap > 1 second between cues
- Preserves timing from start of first to end of second

#### Shift All Timings - Décaler les timings
Offset all cue timings by a specified amount.

**Features:**
- Visual preview with color-coded values (green/red)
- Quick presets: -5s, -2s, -0.5s, +0.5s, +2s, +5s
- Fine-tuning with ±1s and ±0.1s buttons
- Prevents negative time values
- Shows count of affected cues

---

### 🔍 Recherche & Navigation

#### Real-time Cue Search
Find cues instantly by searching their text content.

**Features:**
- Live filtering as you type
- Shows "X / Y cues found" counter
- Yellow highlight on matching text
- Case-insensitive search
- Clear button to reset

#### Go to Cue
Click on any cue in the list to jump directly to that position.

---

### 📊 Statistiques & Validation

#### Stats Panel
Comprehensive statistics about your subtitles.

**Metrics displayed:**
- Total Cues count
- Total Duration
- Average Duration per cue
- Total Words
- Words Per Minute (WPM) with color coding
- Total Characters

#### Validation System
Professional-grade validation with 6 rules.

**Checks:**
| Rule | Threshold | Type |
|------|-----------|------|
| Minimum duration | < 0.5s | Error |
| Maximum duration | > 10s | Warning |
| Line length | > 42 chars | Warning |
| Total length | > 84 chars | Warning |
| Reading speed | > 25 CPS | Error |
| Empty text | No content | Error |

**Visual feedback:**
- Icons on each cue (⚠️ warning, ❌ error)
- Clickable issues to jump to problematic cue
- Color-coded cue borders
- Summary badges in stats panel

---

### 🎨 Interface

#### Theme System - 5 Themes
Customize the editor's appearance.

| Theme | Description |
|-------|-------------|
| 🌙 Dark | Default dark theme |
| ☀️ Light | Light mode for bright environments |
| 💙 Blue | Blue accent theme |
| 💜 Purple | Purple accent theme |
| 🧡 Orange | Orange accent theme |

- Saved to localStorage
- Waveform colors update automatically
- Persists across sessions

#### Editable Markers
Enhanced marker system with customization.

**Features:**
- Double-click marker to edit
- Custom text labels
- 6 color options
- Delete from edit modal
- Visual indicators on waveform

#### Minimap
Global timeline overview for navigation.

**Features:**
- Shows all cues as colored blocks
- Displays all markers
- Playhead indicator
- Click to seek anywhere
- Toggle visibility

---

### 📥 New Import Formats

| Format | Extension | Description |
|--------|-----------|-------------|
| ASS | .ass, .ssa | Advanced SubStation Alpha |
| SBV | .sbv | YouTube subtitle format |
| DFXP | .dfxp, .ttml, .xml | Netflix/Broadcast standard |
| JSON | .json | Complete project backup |

---

### 💾 New Export Formats

| Format | Extension | Use Case |
|--------|-----------|----------|
| VTT | .vtt | Web standard (HTML5 video) |
| SRT | .srt | Universal compatibility |
| ASS | .ass | Advanced styling (anime, karaoke) |
| SBV | .sbv | YouTube uploads |
| DFXP | .dfxp | Netflix, broadcast TV |
| JSON | .json | Full project backup/restore |

**Export dropdown with icons and descriptions:**
```
💾 Export
├─ 📝 VTT - WebVTT Standard web
├─ 🎬 SRT - SubRip Universal
├─ 🎨 ASS - Advanced SubStation Alpha
├─ ▶️ SBV - YouTube Format
├─ 📺 DFXP - TTML Netflix/Broadcast
└─ 📦 JSON - Complete Backup
```

---

## 📦 Installation

### Option 1: Direct Download (Recommended)
1. Download `vtt-editor-pro-v3.0.html`
2. Double-click to open in your browser
3. Start editing!

### Option 2: Use Online Version
Visit: [https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v3.0.html](https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v3.0.html)

### Option 3: Local Server
```bash
# Clone the repository
git clone https://github.com/RDTvlokip/vtt-editor-pro.git
cd vtt-editor-pro

# Open with a local server (optional)
python -m http.server 8000
# Navigate to http://localhost:8000/vtt-editor-pro-v3.0.html
```

---

## 🎯 Quick Start

1. **Import Audio**: Click `📂 Import MP3` to load your audio file
2. **Add Regions**: Click `➕ Add Region` or drag on the timeline
3. **Enable Snap Grid** (optional): Toggle `🧲 Snap Grid` and select interval
4. **Edit Text**: Type your subtitles in the text field
5. **Adjust Timing**: Drag region edges or use Start/End fields
6. **Use Search**: Find specific cues with the search box
7. **Check Stats**: Click `📊 Stats` to view validation
8. **Choose Theme**: Select your preferred color theme
9. **Export**: Click `💾 Export` and choose your format

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Space` | Play/Pause audio |
| `←` | Jump back 1 second |
| `→` | Jump forward 1 second |
| `Ctrl+S` | Mark Start time |
| `Ctrl+E` | Mark End time |
| `Ctrl+Enter` | Add/Update Cue |
| `Ctrl+Z` | Undo (20-step history) |
| `Ctrl+Y` | Redo |
| `Ctrl+F` | Focus search box |
| `M` | Add Marker |
| `Delete` | Delete selected region |

---

## 🎨 Usage Tips

### Working with Multiple Tracks
1. Create new track: Click `🎬 Tracks`
2. Name your track (EN, FR, Music, etc)
3. Edit independently
4. Export each track separately
5. Merge tracks in final video editor

### Using the Validation System
1. Click `📊 Stats` to open statistics panel
2. Review validation warnings and errors
3. Click on any issue to jump to that cue
4. Fix timing or text issues
5. Re-check until all green

### Efficient Editing Workflow
1. Import audio and create rough cues
2. Use **Shift All Timings** to sync with audio
3. Use **Split Cue** for long segments
4. Use **Merge Cues** for fragmented text
5. Run validation check
6. Export in desired format

### Using Search Effectively
1. Type in the search box to filter cues
2. See highlighted matches
3. Click cue to jump and edit
4. Clear search to see all cues

---

## 📚 Advanced Features

### Multi-Track Management
- **Independent timelines** per track
- **Sync control** to keep tracks aligned
- **Track visibility** toggle
- **Export flexibility** (individual or combined)

### Marker System
- **Visual bookmarks** on waveform
- **Custom labels** for organization
- **Color coding** for different marker types
- **Quick navigation** between markers
- **Performance optimized** for 1000+ markers

### Format Support
| Format | Import | Export | Notes |
|--------|--------|--------|-------|
| VTT | ✅ | ✅ | Full WebVTT with color metadata |
| SRT | ✅ | ✅ | SubRip with timing conversion |
| ASS | ✅ | ✅ | Styling stripped on import |
| SBV | ✅ | ✅ | YouTube format |
| DFXP | ✅ | ✅ | TTML/Netflix standard |
| JSON | ✅ | ✅ | Complete project backup |

### Auto-save System
- Saves every **5 seconds** to `localStorage`
- Restores on page reload with confirmation prompt
- Works offline – no cloud required
- Clear with browser cache if needed

### Undo/Redo System
- **20-step history**
- Works with all operations (add, edit, delete, batch, shift, split, merge)
- Keyboard shortcuts: `Ctrl+Z` (undo), `Ctrl+Y` (redo)
- Visual button feedback (disabled when at history limit)

---

## 🗺️ Roadmap

### ✅ v2.1 (Released)
- [x] Visual resize handles with tooltips
- [x] Snap-to-grid alignment
- [x] Batch text editing

### ✅ v2.2 (Released)
- [x] Multi-Track Subtitle Support
- [x] Waveform Markers/Bookmarks
- [x] SRT Export/Import
- [x] Current Time Update
- [x] VTT Import Validation
- [x] Keyboard Shortcut Conflict Resolution
- [x] Waveform Color Update
- [x] Color Persistence in VTT

### ✅ v3.0 (Released)
- [x] Export to ASS, SBV, DFXP, JSON formats
- [x] Import from ASS, SBV, DFXP, JSON formats
- [x] Theme system (5 themes)
- [x] Advanced editing (Split, Merge, Shift)
- [x] Real-time cue search
- [x] Statistics panel with validation
- [x] Editable markers with labels
- [x] Minimap timeline view
- [x] Enhanced dropdown UI

### v3.1 (Planned)
- [ ] Copy/Paste cues (Ctrl+C / Ctrl+V)
- [ ] Go to time - Jump to precise timestamp
- [ ] Custom keyboard shortcuts UI
- [ ] Whisper API integration for auto-transcription

### Desktop Version (Under Consideration)
- [ ] Electron app with offline Whisper
- [ ] Local model support (tiny/base/small/medium)
- [ ] Native FFMPEG integration
- [ ] GPU acceleration for faster processing

---

## 🤝 Contributing

Contributions are welcome! This project is actively maintained.

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Keep it vanilla JS (no frameworks)
- Maintain single-file architecture
- Write clear comments for complex logic
- Test in Chrome, Firefox, and Safari
- Follow existing code style

### Reporting Issues
Found a bug or have a suggestion? [Open an issue](https://github.com/RDTvlokip/vtt-editor-pro/issues)

**Please include:**
- Browser version
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable

---

## 🔧 Technical Details

### Architecture
- **Single HTML file**: All CSS, JS, and HTML in one file (6900+ lines)
- **Vanilla JavaScript**: No build tools, no frameworks
- **WaveSurfer.js v7**: Waveform visualization and audio playback
- **localStorage**: Client-side persistence

### Performance
- **Load time**: <5ms (scripting only)
- **Memory usage**: ~200 MB (depends on audio file size)
- **Max cues tested**: 1000+ without performance issues
- **Max markers tested**: 1000+ without lag
- **Audio formats**: MP3, WAV, OGG, M4A, AAC

### Browser Compatibility
| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Fully supported |
| Firefox | 88+ | ✅ Fully supported |
| Safari | 14+ | ✅ Fully supported |
| Edge | 90+ | ✅ Fully supported |

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)** - see the [LICENSE.md](LICENSE.md) file for details.

### You are free to:
- ✅ **Share**: Copy and redistribute in any medium or format
- ✅ **Adapt**: Remix, transform, and build upon the material

### Under these terms:
- 📝 **Attribution**: Give appropriate credit to the original author
- 🚫 **NonCommercial**: Not for commercial use without permission

**Commercial use requires explicit permission.** Contact me for licensing inquiries.

---

## 🙏 Acknowledgments

- [WaveSurfer.js](https://wavesurfer-js.org/) - Audio waveform visualization library
- Inspired by Aegisub, but built for the modern web
- Community feedback from subtitle editors and content creators

---

## 👤 Author

**RDTvlokip (Théo)**
- 🧬 Creator of [AG-BPE](https://zenodo.org/records/16739553) (Attention-Guided Byte Pair Encoding)
- 🤖 Developer of InfiniGPT model family
- 🎓 TSSR Student specializing in Network Administration
- 🔗 GitHub: [@RDTvlokip](https://github.com/RDTvlokip)

---

## ☕ Support

If VTT Editor Pro helps you, consider supporting the project:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?style=for-the-badge&logo=buy-me-a-coffee)](https://ko-fi.com/rdtvlokip)

Your support helps maintain and improve this tool!

---

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/RDTvlokip/vtt-editor-pro?style=social)
![GitHub forks](https://img.shields.io/github/forks/RDTvlokip/vtt-editor-pro?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/RDTvlokip/vtt-editor-pro?style=social)

---

**Built with ❤️ using vanilla JavaScript**

[🐛 Report Bug](https://github.com/RDTvlokip/vtt-editor-pro/issues) • [✨ Request Feature](https://github.com/RDTvlokip/vtt-editor-pro/issues) • [📖 Documentation](https://github.com/RDTvlokip/vtt-editor-pro/wiki)

---

## 🌟 Star History

If you find this project useful, please consider giving it a ⭐ on GitHub!

---

<div align="center">

### Made with passion for subtitle editors worldwide 🌍

*No ads • No tracking • No subscriptions • Just pure functionality*

</div>
