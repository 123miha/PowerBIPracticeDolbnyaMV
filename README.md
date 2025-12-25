# 🎭 VRM Motion Capture Studio

<div align="center">

![React](https://img.shields.io/badge/React-18.x-61dafb?style=for-the-badge&logo=react&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-0.160+-black?style=for-the-badge&logo=three.js&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Holistic-4285f4?style=for-the-badge&logo=google&logoColor=white)
![VRM](https://img.shields.io/badge/VRM-1.0-ff69b4?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Real-time face, body, and hand motion capture with live VRM avatar control**

[Demo](https://your-demo-link.vercel.app) • [Documentation](docs/) • [Report Bug](https://github.com/your-username/vrm-mocap/issues) • [Request Feature](https://github.com/your-username/vrm-mocap/issues)

![Demo Screenshot](https://via.placeholder.com/800x400?text=Add+Your+Demo+Screenshot+Here)

</div>

---

## 📋 Table of Contents

- [About](#about)
- [Key Features](#-key-features)
- [Demo](#-demo)
- [Quick Start](#-quick-start)
- [Usage](#-usage)
- [Performance](#-performance)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## About

VRM Motion Capture Studio is a browser-based application that transforms your webcam into a professional motion capture system. Using cutting-edge AI and computer vision, it tracks 478 facial landmarks, 33 body points, and 42 hand landmarks to animate your VRM avatar in real-time with stunning accuracy.

Perfect for VTubers, content creators, game developers, and anyone interested in accessible motion capture technology.

### Why This Project?

- ✅ **No expensive hardware** — just a webcam and browser
- ✅ **Runs entirely in-browser** — no server or installation required
- ✅ **Open source and free** — MIT licensed
- ✅ **Production-ready** — optimized for 60 FPS performance

---

## ✨ Key Features

### 🎯 Motion Capture
- **Facial tracking** — 478 points capturing mouth shapes (A, I, U, E, O), eye blinks, gaze direction, and head rotation
- **Body tracking** — 33 points for shoulders, arms, torso, and posture
- **Hand tracking** — 21 points per hand with enhanced finger curl detection (1.3x multiplier)

### 🎨 Customization
- **VRM avatar support** — drag-and-drop .vrm file loading
- **Expression presets** — Happy, Sad, Angry, Surprised, Relaxed
- **10 HDRI environments** — Dark, Night, Sunset, Studio, Forest, and more
- **Debug tools** — position, rotation, scale controls with grid overlay

### 📊 Performance Tools
- **Real-time metrics** — FPS counter, latency monitor, detection quality
- **Optimization options** — adjustable smoothing, model complexity
- **Test mode** — comprehensive performance analysis

---

## 🎬 Demo

### Live Application
👉 **[Try it now](https://your-demo-link.vercel.app)**

### Video Demonstration
📺 **[Watch on YouTube](https://youtube.com/your-demo-video)**

### Screenshots

<details>
<summary>Click to expand</summary>

![Main Interface](https://via.placeholder.com/600x400?text=Main+Interface)
*Main capture interface with avatar and controls*

![Expression Control](https://via.placeholder.com/600x400?text=Expression+Control)
*Expression preset selection*

![Performance Metrics](https://via.placeholder.com/600x400?text=Performance+Metrics)
*Real-time performance monitoring*

</details>

---

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18.0 or higher
- **Modern browser** (Chrome 90+, Firefox 88+, Edge 90+)
- **Webcam** with 720p+ resolution recommended

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/vrm-mocap.git
cd vrm-mocap

# Install dependencies
npm install

# Start development server
npm run dev
```

The application will open at `http://localhost:5173`

### First Steps

1. **Load an avatar**: Drag a `.vrm` file into the browser or click "Choose File"
   - Download free avatars from [VRoid Hub](https://hub.vroid.com) or [Booth.pm](https://booth.pm/en/search/VRM)
2. **Start capture**: Click the camera button 📷 and allow webcam access
3. **Adjust settings**: Use the sidebar to customize expressions, environment, and debug options

---

## 📖 Usage

### Interface Overview

| Tab | Description |
|-----|-------------|
| 👤 **Avatar** | Load VRM files, access avatar resources |
| 😊 **Expression** | Select facial expressions (Happy, Sad, Angry, Surprised, Relaxed) |
| 🌄 **Scene** | Choose from 10 HDRI environments |
| ⚙️ **Debug** | Adjust position, rotation, scale, and grid display |
| 📊 **Test** | View performance metrics and run tests |

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Toggle camera on/off |
| `E` | Cycle expressions |
| `G` | Toggle debug grid |
| `R` | Reset avatar position |

### Advanced Configuration

For detailed configuration options, see [DEVELOPER_GUIDE.md](docs/DEVELOPER_GUIDE.md).

---

## ⚡ Performance

### Target Metrics

| Metric | Target | Acceptable |
|--------|--------|------------|
| **Frame Rate** | 60 FPS | 30+ FPS |
| **Latency** | <33ms | <100ms |
| **Detection Accuracy** | 95%+ | 80%+ |

### Optimization Techniques

- Frame-rate independent animation with delta time
- Exponential smoothing for natural movement (configurable damping)
- High-resolution camera input (1280×720)
- Optimized MediaPipe settings (model complexity: 1)
- Three.js object pooling and reuse

### Tracking Accuracy

- **Face**: 478 landmarks with refined facial features
- **Body**: 33 landmarks with smooth interpolation
- **Hands**: 42 landmarks (21 per hand) with enhanced finger detection

---

## 🛠️ Tech Stack

### Core Framework
- **[React](https://react.dev)** 18.x — UI library
- **[Three.js](https://threejs.org)** 0.160+ — 3D rendering engine
- **[React Three Fiber](https://docs.pmnd.rs/react-three-fiber)** — React renderer for Three.js
- **[React Three Drei](https://github.com/pmndrs/drei)** — Useful helpers for R3F

### Motion Capture
- **[MediaPipe Holistic](https://google.github.io/mediapipe/solutions/holistic.html)** — Face, body, and hand detection
- **[Kalidokit](https://github.com/yeemachine/kalidokit)** — Pose to VRM mapping and inverse kinematics

### VRM Support
- **[@pixiv/three-vrm](https://github.com/pixiv/three-vrm)** — VRM file loading and animation

### Tooling
- **[Zustand](https://github.com/pmndrs/zustand)** — Lightweight state management
- **[Vite](https://vitejs.dev)** — Fast build tool and dev server

---

## 📁 Project Structure

```
vrm-mocap/
├── public/
│   └── models/              # Default VRM avatars
├── src/
│   ├── components/
│   │   ├── CameraWidget.jsx # Camera capture + MediaPipe integration
│   │   ├── Experience.jsx   # 3D scene setup
│   │   ├── UI.jsx           # User interface and controls
│   │   └── VRMAvatar.jsx    # VRM loading and animation
│   ├── hooks/
│   │   ├── useVideoRecognition.js  # Camera state management
│   │   └── usePerformanceMetrics.js # Performance tracking
│   ├── App.jsx              # Main application component
│   ├── main.jsx             # Entry point
│   └── index.css            # Global styles
├── docs/
│   ├── USER_GUIDE_RU.md     # User guide (Russian)
│   └── DEVELOPER_GUIDE.md   # Developer documentation (English)
├── package.json
├── vite.config.js
└── README.md
```

---

## 🔧 Configuration

### MediaPipe Settings

```javascript
holistic.setOptions({
  modelComplexity: 1,              // 0=lite, 1=full, 2=heavy
  smoothLandmarks: true,           // Enable temporal smoothing
  minDetectionConfidence: 0.5,     // Detection threshold
  minTrackingConfidence: 0.5,      // Tracking threshold
  refineFaceLandmarks: true,       // Enhanced face mesh
});
```

### Animation Damping

```javascript
const DAMPING = {
  face: 0.5,      // Facial expression smoothing
  body: 0.4,      // Body movement smoothing
  arms: 0.5,      // Arm movement smoothing
  hands: 0.6,     // Hand position smoothing
  fingers: 0.7,   // Finger curl smoothing
};
```

### Camera Resolution

```javascript
video: {
  width: { ideal: 1280 },
  height: { ideal: 720 },
  facingMode: "user"
}
```

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

1. **Fork** the repository
2. **Create** your feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow the existing code style
- Add comments for complex logic
- Update documentation for new features
- Test thoroughly before submitting

### Good First Issues

Looking for beginner-friendly tasks? Check out issues labeled [`good first issue`](https://github.com/your-username/vrm-mocap/labels/good%20first%20issue).

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

## 🙏 Acknowledgments

Special thanks to these amazing projects and communities:

- **[VRoid Hub](https://hub.vroid.com)** — Free VRM avatar library
- **[MediaPipe](https://google.github.io/mediapipe)** — Google's ML framework for pose detection
- **[Kalidokit](https://github.com/yeemachine/kalidokit)** — Kinematics solver for VTubing
- **[Pixiv](https://github.com/pixiv/three-vrm)** — three-vrm library maintainers
- **[Pmndrs](https://github.com/pmndrs)** — React Three Fiber and Drei creators
- **[Wawa Sensei](https://wawasensei.dev)** — VRM tutorial inspiration

---

## 📞 Contact & Support

- **Issues**: [GitHub Issues](https://github.com/your-username/vrm-mocap/issues)
- **Discussions**: [GitHub Discussions](https://github.com/your-username/vrm-mocap/discussions)
- **Documentation**: [Full Docs](docs/)

---

<div align="center">

</div>
