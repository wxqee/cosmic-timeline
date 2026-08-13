# Cosmic Timeline Animation

A small looping animation for a science-outreach page that walks through the cosmic timeline.

## Features

- **Inflation**: A single bright point flashes and rapidly inflates outward
- **CMB**: Cooling into a speckled microwave-background haze with cool blue-purple tones
- **First Stars**: Stars and galaxies fade in with a staggered rhythm, forming a 4-arm spiral galaxy
- ~10 second per cycle, loops seamlessly
- Dark-themed with calm pacing
- Self-contained single HTML file

## Tech Stack

- [Three.js r128](https://cdnjs.com/libraries/three.js/r128) — WebGL rendering
- [TWEEN.js 18.6.4](https://github.com/tweenjs/tween.js) — Animation tweening
- Custom GLSL shaders for particle morphing
- Pure HTML5 Canvas + CSS, zero build step

## Usage

Open `index.html` directly in a browser, or serve with any static server:

```bash
python3 -m http.server 8090
# Visit http://localhost:8090/index.html
```

## How It Works

A single particle system (16,384 particles) morphs between two position modes:

1. **CMB scattered positions** — particles uniformly distributed in 3D space using spherical scatter + sqrt distribution
2. **Galaxy spiral positions** — particles arranged in a 4-arm spiral using parametric arm equations

Each particle has an independent `starDelay` so they transition from CMB to galaxy at staggered times, simulating stars igniting at various locations before organizing into a galaxy structure.

## Credits

Based on [foretoo's 3D Galaxy Particles](https://codepen.io/foretoo/pen/zYjpYad) on CodePen, adapted for the cosmic timeline animation.

## License

MIT
