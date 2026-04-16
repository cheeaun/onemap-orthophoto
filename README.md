# OneMap Orthophoto

A web application that renders Singapore's OneMap Orthophoto (satellite) tiles using [MapLibre GL JS](https://maplibre.org/), featuring a custom WebGL post-processing layer for real-time image enhancement.

## ✨ Features

* **Singapore Satellite Imagery:** Integrates directly with OneMap's Orthophoto tile service.
* **Real-time WebGL Enhancements:** Adjust the visual quality of the satellite imagery on the fly using custom WebGL shaders:
  * Noise Reduction
  * Sharpening
  * Brightening
  * Contrast
  * Saturation
* **Smart Presets & Persistence:** Includes a "Best Effort" preset for quick optimization. Your custom settings are automatically saved to `localStorage` and restored on your next visit.
* **Retina/HiDPI Support:** Automatically detects high-density displays and adjusts tile sizes and zoom levels for the crispest possible imagery.
* **Performance Optimized:** The WebGL post-processing layer automatically disables itself when all settings are at their default (zero) to save GPU cycles.

## 🛠️ Tech Stack

* **MapLibre GL JS** - Open-source interactive map library.
* **WebGL** - Custom fragment shaders for real-time image manipulation.
* **Vite 8** - Next-generation frontend tooling for fast builds and development.

## 🚀 Getting Started

### Prerequisites

* Node.js (v18 or higher recommended)
* npm

### Installation

1. Clone the repository and navigate to the project directory.
2. Install the dependencies:

```bash
npm install
```

### Development

Start the Vite development server:

```bash
npm run dev
```

The application will be available at `http://localhost:3000`.

### Production Build

Build the application for production:

```bash
npm run build
```

The optimized static files will be generated in the `dist` directory, ready to be served by any static file server.

## 🙏 Acknowledgments

* Map data &copy; [OneMap](https://www.onemap.gov.sg/)
* Map data &copy; [Singapore Land Authority (SLA)](https://www.sla.gov.sg/)
