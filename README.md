# 🎵 Real-time Audio Frequency Analyzer

A professional-grade **Real-Time Analyzer (RTA)** and **Spectrogram** web application built with the Web Audio API. Analyze audio frequencies in real-time with octave band analysis, musical note detection, and more.

![Audio Analyzer Screenshot](screenshot.png)

## ✨ Features

### 📊 Visualization
- **RTA (Real-Time Analyzer)** - Bar or line graph showing frequency levels
- **Spectrogram** - Waterfall display showing frequency over time
- **SPL History Graph** - 60-second trend of sound pressure level

### 🎛️ Analysis Controls
| Control | Description |
|---------|-------------|
| **Resolution** | 1/1 to 1/48 octave band analysis |
| **Weighting** | Z (flat), A-weight, C-weight |
| **FFT Size** | 1024 to 16384 samples |
| **Response** | Fast (125ms), Slow (1s), Impulse (35ms) |
| **Smoothing** | Adjustable time constant |

### 🎵 Measurement Features
- **Musical Note Detection** - Shows note name (A4, C#5) with cents deviation
- **Peak Frequency** - Real-time peak frequency and dB level
- **SPL Display** - Broadband sound pressure level
- **Max Hold** - Peak level memory line
- **Dynamic Y-Axis** - Auto-scales to signal level

### 🔧 Tools
- **📷 Screenshot** - Export RTA + Spectrogram as PNG
- **⏸️ Freeze** - Pause display for analysis
- **🔊 Noise Generator** - White/Pink noise for calibration
- **🎚️ Mic Calibration** - dB offset for calibrated readings

## 🚀 Quick Start

### Option 1: Open Locally (recommend)
1. Download or clone this repository
2. Open `index.html` in a modern browser (Chrome, Firefox, Edge)
3. Click **Start** and allow microphone access

### Option 2: Online
Visit url: https://qphugit.github.io/audio-analyzer/

## 📖 User Guide

### Basic Usage
1. Click **Start** to begin audio capture
2. Allow microphone permission when prompted
3. Speak or play audio to see the frequency response

### Understanding the Display

#### RTA (Top Panel)
- **X-axis**: Frequency (20 Hz - 20 kHz, logarithmic)
- **Y-axis**: Level in dB
- **Bars/Line**: Current frequency levels
- **Pink Line**: Max Hold (if enabled)
- **Yellow Marker**: Peak frequency

#### Spectrogram (Bottom Panel)
- **X-axis**: Frequency (matches RTA)
- **Y-axis**: Time (newest at top, scrolls down)
- **Colors**: Blue (quiet) → Cyan → Green → Yellow → Red → White (loud)

### Controls Reference

| Control | Purpose |
|---------|---------|
| 📷 | Save screenshot |
| ⏸️ | Freeze/Resume display |
| **Response** | Measurement speed |
| **Noise Gen** | Test signal generator |
| **Resolution** | Frequency detail level |
| **Weighting** | Frequency weighting curve |
| **Display** | Bar or Line mode |
| **Max Hold** | Show peak levels |
| **SPL Graph** | Show/hide SPL history |
| **Mic Cal** | Calibration offset (dB) |
| **Spec Height** | Spectrogram size ratio |
| **Smoothing** | Display smoothness |
| **FFT Size** | Frequency resolution |

### Calibration
To calibrate with a reference SPL meter:
1. Play a steady tone or pink noise
2. Read the reference meter value
3. Note the app's displayed value
4. Enter the difference in **Mic Cal (dB)**

Example: If reference shows 85 dB and app shows -45 dB:
```
Calibration = 85 - (-45) = 130 dB
```

## 🔒 Browser Requirements

- **Modern browser**: Chrome 66+, Firefox 60+, Edge 79+, Safari 14.1+
- **HTTPS required**: Microphone access requires secure context
- **Permissions**: Must allow microphone access

## 📝 Technical Notes

- Uses Web Audio API `AnalyserNode` for FFT analysis
- FFT window function: Blackman-Harris (browser default)
- Sample rate: Determined by system (typically 44.1kHz or 48kHz)
- Display refresh: ~60 FPS via `requestAnimationFrame`

## 📄 License

MIT License - Free for personal and commercial use.

## 👤 Author

**QuocPhu**
- Telegram: [@Phu_Data](https://t.me/Phu_Data)
- Facebook: [QuocPhu47](https://fb.com/QuocPhu47)

---

Made with ❤️ using Web Audio API


