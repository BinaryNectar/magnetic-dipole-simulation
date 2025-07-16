# Magnetic Dipole Field Simulation

A 3D web visualization of magnetic field lines around a dipole (bar magnet) using Three.js.

## Overview

This project renders a rotating 3D simulation of magnetic field lines emanating from a dipole moment. The field lines are traced by numerical integration of the dipole field equation and colored red (positive pole) and blue (negative pole).

## Demo

1. Serve the project over HTTP to avoid CORS issues (e.g., using Python’s built-in server).
2. Navigate to `http://localhost:8000/index.html` in a modern browser with ES module support.
3. Use mouse drag and scroll to orbit, pan, and zoom the scene (OrbitControls).

## Features

* **Dipole field calculation:** Implements the magnetic dipole equation to compute field vectors.
* **Field line tracing:** Integrates along the field direction to draw smooth lines.
* **Interactive camera:** Rotate and zoom with Three.js `OrbitControls`.
* **Auto-rotation:** Continuous slow rotation of the scene for an engaging view.
* **Responsive canvas:** Automatically resizes on window changes.

## Prerequisites

* A modern web browser (Chrome, Firefox, Edge, Safari) supporting ES modules.
* Static file server (e.g., Python 3.x, Node.js `http-server`).

## Installation & Setup

```bash
# Clone the repository (or copy files)
git clone https://github.com/binarynectar/magnetic-dipole-simulation.git
cd magnetic-dipole-simulation

# Start a local server (Python example)
python3 -m http.server 8000
```

## Usage

* Open `index.html` via `http://localhost:8000/index.html`.
* Drag to rotate the camera, scroll to zoom.
* Observe red lines tracing from the positive pole and blue lines from the negative pole.

## File Structure

```text
└── index.html      # Main simulation entry point
```

## Configuration

Within the `<script type="module">` block in `index.html`, you can adjust:

| Variable                   | Description                             |
| -------------------------- | --------------------------------------- |
| `dipoleMoment`             | Vector direction/strength of the dipole |
| `radius` (in draw)         | Starting circle radius for field lines  |
| `steps`                    | Maximum integration steps per line      |
| `stepSize`                 | Step length for field-line integration  |
| `controls.autoRotateSpeed` | Speed of auto-rotation control          |

Tweak these values to explore different field geometries.

## Dependencies

* **Three.js 0.160.0** via import map from UNPKG
* **OrbitControls** addon for camera interaction
* **es-module-shims v1.8.0** for import map support

## Contributing

1. Fork the repo.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit changes (`git commit -m "Add YourFeature"`).
4. Push to your branch and open a Pull Request.

## License

This project is released under the MIT License. Feel free to use and modify as desired.
