# Google Model Viewer Interactive Showcase & Guide

A premium, minimal, and fully interactive single-page website showcasing Google's `<model-viewer>` web component. The project is designed with a **Premium Light Studio** layout to optimize shadow visualization and readability for 3D web designers.

The page includes a live 3D sandbox playground, comprehensive documentation guides, and responsive layout styling optimized for mobile, tablet, and desktop devices.

## 🚀 Live Demo & Hosting
The repository is hosted at:
[https://github.com/Denzils-repo/showcasing_modelviewer](https://github.com/Denzils-repo/showcasing_modelviewer/)

---

## ⚡ Features
1. **Interactive Hero Studio**: View the 3D treasure chest model (`chest.glb`) rendered in a virtual light studio. Move, scale, and pan the model freely.
2. **Interactive Configuration Sandbox**: Adjust lighting exposure, shadow intensity, shadow softness, auto-rotation, and camera controls in real-time.
3. **Live Code Exporter**: Real-time auto-generated HTML code matching the custom configuration of the playground with a copy-to-clipboard button.
4. **Mobile & AR Optimized**: Responsive layout with touch-friendly controls. Includes a mobile-only **Launch AR Mode** capability that programmatically places the 3D model into your physical room using ARCore (Android) or AR Quick Look (iOS).
5. **3D Asset Source Directory**: Detailed listings and direct links to sketchfab, Poly Haven, and CGTrader for downloading high-quality 3D assets.

---

## 🛠️ How to Run Locally

To view the showcase locally, spin up any local HTTP server in this directory:

### Option A: Using Node.js (http-server)
1. Install the server globally or run it via npx:
   ```bash
   npx http-server -c-1
   ```
   *(Note: `-c-1` disables browser caching so you can see styling edits in real-time).*
2. Open `http://localhost:8080/index.html` in your browser.

### Option B: Python Server
If you have Python installed, run:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000/index.html`.

---

## 📦 Repository Structure
```
├── index.html     # Main interactive website
├── chest.glb      # 3D treasure chest model asset
└── README.md      # Documentation
```

---

## ⚙️ Requirements for Mobile AR in Production
For the **Launch AR Mode** button to function successfully in your deployed project:
1. **HTTPS Context**: The page must be hosted over a secure HTTPS connection. Mobile browsers block access to camera and motion sensors on standard HTTP connections.
2. **CORS Configuration**: The 3D model files must be hosted on the same origin or configured with appropriate Cross-Origin Resource Sharing (CORS) headers.
3. **Device Support**: The mobile device must support Google ARCore (Android) or Apple ARKit (iOS).
