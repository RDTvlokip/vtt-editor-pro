# 🎵 VTT Editor Pro v2.2

🚀 **[Try it online → https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v2.2.html](https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v2.2.html)**

A modern, lightweight, and powerful WebVTT subtitle editor that runs entirely in your browser. No installation, no signup, no cloud dependencies – just one HTML file.

**Clean starting point:**
![VTT Editor Pro v2.2 - Empty State](screenshot-empty.png)

**In action with live preview:**
![VTT Editor Pro v2.2 - Active Editing](screenshot-active.png)

---

## ✨ Features

### 🎨 **Modern Interface**
- Clean, dark-themed UI designed for extended editing sessions
- Color-coded regions for easy organization
- Real-time waveform visualization
- Responsive timeline with zoom controls
- **NEW:** Enhanced visual resize handles with real-time tooltips

### ⚡ **Powerful Editing**
- **Drag & Drop**: Move and resize regions directly on the timeline
- **Visual Resize Handles**: See exact timestamps while resizing regions
- **Snap-to-Grid**: Align regions precisely with configurable intervals (10ms to 1s)
- **Batch Text Editing**: Transform multiple cues at once with Find & Replace, case transformations, and prefix/suffix tools
- **Anti-overlap Enforcement**: Optional feature to prevent subtitle collisions
- **Live Preview**: Scrolling lyrics display synchronized with playback
- **Auto-save**: Your work is saved every 5 seconds (localStorage)

### 🎯 **Workflow Optimized**
- Import MP3/audio files directly
- Import/Export WebVTT and SRT formats
- Keyboard shortcuts for rapid editing
- Precise timestamp control with snap-to-grid
- Visual waveform for accurate timing
- Undo/Redo with 20-step history

### 🚀 **Technical Highlights**
- **3570 lines** of vanilla JavaScript – no frameworks
- **~200 MB RAM** usage
- **Offline-first**: Works without internet connection
- **Single file**: Just download and open in your browser
- Zero external dependencies (except WaveSurfer.js CDN)
- **Support for 1000+ cues and markers without lag**

---

## 🆕 What's New in v2.2

### 1. 🎬 Multi-Track Subtitle Support
Manage multiple subtitle tracks simultaneously. Organize different languages, speaker tracks, or subtitle styles in parallel without conflicts.

**How it works:**
- Create multiple tracks with independent timelines
- Switch between tracks seamlessly
- Export each track separately
- Keep all tracks in sync with the same audio

**Use cases:**
- Multi-language projects (EN, FR, DE tracks)
- Dialogue + Music + SFX subtitles
- Different subtitle styles for same content

### 2. 🎯 Waveform Markers/Bookmarks
Mark important moments in your audio timeline. Create visual bookmarks for beats, dialogue starts, or key events.

**Features:**
- Add markers at any point on the waveform
- Color-code markers for organization
- Jump to marker with one click
- Export/Import marker positions
- Support for 1000+ markers without performance impact

### 3. 📥 SRT Export/Import
Full compatibility with SRT (SubRip) format. Import existing SRT files or export your subtitles in SRT format.

**Features:**
- Automatic format conversion VTT ↔ SRT
- Preserves timing and text
- Option to choose format on export
- Clean SRT parsing with validation

**SRT Format:**
```
1
00:00:12,620 --> 00:00:13,160
Yeah.

2
00:00:14,740 --> 00:00:15,101
Yeah.
```

### 4. ⏱️ Current Time Update
Real-time sync with audio playback. The current time display updates live as audio plays.

**Features:**
- Shows current playback position
- Highlighted cue indicator
- Jump to specific cue instantly
- Perfect for real-time subtitle verification

### 5. ✅ VTT Import Validation
Validate VTT files before importing. Catch formatting errors, invalid timestamps, and malformed cues.

**Detects:**
- Invalid time format (must be HH:MM:SS.mmm)
- Overlapping cues (optional)
- Missing text content
- Malformed headers
- Duplicate cue IDs

**Feedback:**
- Shows error count
- Specifies line number of errors
- Suggests fixes

### 6. ⌨️ Keyboard Shortcut Conflict Resolution
Intelligent keyboard shortcut system that prevents conflicts and ensures smooth workflow.

**Features:**
- Smart shortcut assignment
- Conflict detection
- Alternative shortcuts for common actions
- Customizable shortcuts (future release)

**Enhanced Shortcuts:**
```
Space          → Play/Pause
←/→            → Jump ±1 second
Ctrl+S         → Mark Start
Ctrl+E         → Mark End
Ctrl+Enter     → Add/Update Cue
Ctrl+Z/Y       → Undo/Redo
Delete         → Delete Region
Ctrl+B         → Batch Edit
Ctrl+M         → Add Marker
```

### 7. 🎨 Waveform Color Update
Enhanced waveform visualization with improved color contrast and clarity.

**Improvements:**
- Better color distinction between tracks
- Adjusted opacity for better visibility
- Custom waveform colors per track
- High-contrast mode for accessibility

### 8. 💾 Color Persistence in VTT
Your color assignments are now saved **directly in the VTT file** using a custom format.

**Format:**
```
WEBVTT

cue-1 [color: #20bf6b]
00:00:12.620 --> 00:00:13.160
Yeah.

cue-2 [color: #feca57]
00:00:14.740 --> 00:00:15.101
Yeah.
```

**Features:**
- Colors persist across export/import
- Standard VTT players ignore custom syntax (100% compatible)
- Unique color per cue
- Auto-generate random colors if not specified

---

## 📦 Installation

### Option 1: Direct Download (Recommended)
1. Download `vtt-editor-pro-v2.2.html`
2. Double-click to open in your browser
3. Start editing!

### Option 2: Use Online Version
Visit: [https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v2.2.html](https://rdtvlokip.github.io/vtt-editor-pro/vtt-editor-pro-v2.2.html)

### Option 3: Local Server
```bash
# Clone the repository
git clone https://github.com/RDTvlokip/vtt-editor-pro.git
cd vtt-editor-pro

# Open with a local server (optional)
python -m http.server 8000
# Navigate to http://localhost:8000/vtt-editor-pro-v2.2.html
```

---

## 🎯 Quick Start

1. **Import Audio**: Click `📂 Import MP3` to load your audio file
2. **Add Regions**: Click `➕ Add Region` or drag on the timeline
3. **Enable Snap Grid** (optional): Toggle `🧲 Snap Grid` and select interval
4. **Edit Text**: Type your subtitles in the text field
5. **Adjust Timing**: Drag region edges (watch the tooltip!) or use Start/End fields
6. **Add Markers** (optional): Click on waveform to add bookmarks
7. **Use Batch Edit** (optional): Click `📝 Batch Edit` for bulk operations
8. **Choose Format**: Export as VTT or SRT
9. **Export**: Click `💾 Export` to save your file

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
| `Ctrl+B` | Open Batch Edit |
| `Ctrl+M` | Add Marker |
| `Delete` | Delete selected region |

---

## 🎨 Usage Tips

### Working with Multiple Tracks
1. Create new track: `➕ New Track`
2. Name your track (EN, FR, Music, etc)
3. Edit independently
4. Export each track separately
5. Merge tracks in final video editor

### Using Markers for Organization
1. Click on waveform to add marker
2. Assign color to marker
3. Use markers as visual cues
4. Jump between markers with shortcuts
5. Export marker data with subtitle file

### Import/Export Workflow
1. **Import:** Drag & drop VTT or SRT file
2. **Validate:** App checks for errors
3. **Edit:** Make your changes
4. **Export:** Choose VTT or SRT format
5. **Save:** Colors and timing preserved

### Color Persistence
- Colors are embedded in VTT file
- Works with any VTT player (ignores custom syntax)
- Reimport file = colors auto-restore
- No separate color file needed

### Snap-to-Grid Workflow
1. Enable `🧲 Snap Grid` toggle
2. Select interval (e.g., 100ms for music)
3. Resize/move regions – they snap automatically
4. Disable when you need pixel-perfect control

### Batch Editing Workflow
1. Create all your cues with timing
2. Click `📝 Batch Edit`
3. Use **Find & Replace** to fix typos globally
4. Use **Transform** to apply consistent casing
5. Use **Modify** to add symbols or formatting

---

## 📚 Advanced Features

### Multi-Track Management
- **Independent timelines** per track
- **Sync control** to keep tracks aligned
- **Track visibility** toggle
- **Export flexibility** (individual or combined)
- **Merge option** for final export

### Marker System
- **Visual bookmarks** on waveform
- **Color organization** for different marker types
- **Quick navigation** between markers
- **Marker export** with cue data
- **Performance optimized** for 1000+ markers

### Format Support
- **VTT**: Full WebVTT specification
- **SRT**: SubRip format with conversion
- **Custom metadata**: Color codes in standard VTT
- **Validation**: Error detection on import

### Auto-save System
- Saves every **5 seconds** to `localStorage`
- Restores on page reload with confirmation prompt
- Works offline – no cloud required
- Clear with browser cache if needed

### Undo/Redo System
- **20-step history**
- Works with all operations (add, edit, delete, batch, markers)
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

### v3.0 (Planned)
- [ ] Zero-dependency edition (remove WaveSurfer.js)
- [ ] Whisper API integration for auto-transcription
- [ ] FFMPEG.js for video support
- [ ] Export to ASS, SBV, DFXP formats
- [ ] Custom keyboard shortcuts UI
- [ ] Theme system (light/dark/custom)

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
- **Single HTML file**: All CSS, JS, and HTML in one file (3570 lines)
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
