# Interactive Birthday Card Project

A highly interactive, web-based birthday card experience featuring 3D CSS transformations, HTML5 Canvas particle physics, and advanced text masking effects.

## 🌟 Features

* **3D Cylinder Intro:** A rotating 3D text cylinder that builds anticipation before the card reveal.
* **Particle Assembly Effect:** The main photo  is generated using HTML5 Canvas particles that fly in from scattered positions to assemble the image like a jigsaw puzzle.
* **Interactive Jigsaw:** Tapping the photo frame "breaks" the puzzle, scattering the particles, which then re-assemble automatically.
* **Split-Text Reveal:** The "Thank You" message features a CSS clip-path animation that splits open to reveal a hidden "For Everything" message on click/hover.
* **Text Masking:** The main title utilizes background-clip text masking with a dynamic moving texture.
* **Responsive Design:** Optimized for both desktop and mobile viewing (including touch support).

## 📂 Project Structure

* `index.html` - The main entry point containing HTML, CSS, and JavaScript.
* `uncle.jpg` - The photo to be displayed in the frame (required).
* `background.png` - The living room background image (required).

## 🚀 How to Run

1.  Ensure `index.html`, `uncle.jpg`, and `background.png` are in the same folder.
2.  Open `index.html` in any modern web browser (Chrome, Firefox, Safari).
    * *Note: Due to browser security policies (CORS), image pixel manipulation might require running a local server (like Live Server in VS Code) rather than just double-clicking the file.*

## 🎨 Credits & Attributions

**Photography & Assets:**
* **Text Masking Texture:** [Photo by Conor Sexton on Unsplash](https://unsplash.com/@conorsexton).
* **Background & Frame:** Custom generated / Local assets.

**Inspiration & Techniques:**
* **CSS Text Animations:** Techniques adapted from [Prismic.io CSS Text Animations Guide](https://prismic.io/blog/css-text-animations).
* **Particle Physics:** Custom HTML5 Canvas implementation using standard velocity/friction logic.

## 🛠️ Configuration

You can tweak the animation settings in the `CONFIG` object inside `index.html`:

```javascript
const CONFIG = {
    introDuration: 5000,    // Time the 3D intro spins (ms)
    particleSize: 3,        // Size of image particles (px)
    scanStep: 3,            // Density of particles (higher = better performance, lower quality)
    assembleSpeed: 0.02,    // Speed of particle flight (0.01 - 1.0)
};
```