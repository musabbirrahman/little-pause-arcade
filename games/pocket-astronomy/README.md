# 🔭 Pocket Astronomy: Edu Edition

A relaxing, single-file browser game where you pilot a telescope through real space, scan and log 42 real (and theoretical) objects, and learn real astronomy along the way. It runs on phones, tablets and desktops with no install and no dependencies.

> Drag across the sky, line an object up in the reticle, capture it, and read how astronomers actually know what they know.

## Features

- **42 objects across 6 sectors:** from the Hubble Telescope and ISS in Earth orbit, through every planet and major moon, to red supergiants, nebulae, black holes, galaxies and quasars.
- **Realistic rendering:** procedural planet surfaces wrapped on rotating spheres, lit from one side; Jupiter's Great Red Spot; layered rings on Saturn (with shadow on the planet); spiral galaxies; black holes with a photon ring; spectral-class star colours and a Milky Way band.
- **Real learning built into every discovery:**
  - temperature, gravity, size, mass and distance
  - **light-travel time** ("you see it as it was X years ago")
  - **size compared with Earth**
  - **Why this sensor?** (why radio, infrared, X-ray or UV reveals this object)
  - **How we know** (spectroscopy, Kepler's third law, standard candles, the Event Horizon Telescope images)
- **Sky guide:** 7 real constellations (Orion, Big Dipper, Cassiopeia, Southern Cross, Scorpius, Lyra, Cygnus) with 40 selectable stars. Tap a star, or centre it in the reticle and press **Study**, to read its spectral class, temperature and distance.
- **Mission quiz:** questions generated from what you have scanned and studied (which is farther, how long light takes to arrive, which star is hotter, which constellation).
- **Photo mode:** save a shareable card of any object, with its picture and key data, as a PNG. On phones that support it, the share sheet opens.
- **Generative ambient music** and sound effects, with a mute button that remembers your choice.
- **Mobile-first layout:** large touch targets, bottom-sheet data pads, safe-area support, landscape mode, haptic taps, and a reduced star count on small screens for smooth performance.
- **Progress saved automatically** in your browser, with a backup/restore box and a reset button.

## How to play

1. **Scan:** drag to pan the sky. Zoom with the **+ / −** buttons, pinch (touch) or the mouse wheel.
2. **Lock on:** line an object up in the central reticle. If you are using the right sensor, a **Capture** button appears.
3. **Equip:** some objects only show up in certain wavelengths. Buy sensor packs and switch between them to decode what you find.
4. **Learn:** open the data pad to read the facts, then log it to your database.
5. **Upgrade:** spend grants on better telescopes to reach deeper sectors.

### Sectors

| # | Sector | Needs |
|---|--------|-------|
| 1 | Earth Orbit | start |
| 2 | Inner Solar System | 5 discoveries |
| 3 | Outer Giants | 11 discoveries |
| 4 | The Milky Way | 17 discoveries |
| 5 | Deep Universe | 24 discoveries |
| 6 | The Theoretical Edge | 29 discoveries |

The Theoretical Edge holds hypothetical objects (white holes, wormholes, Dyson spheres and others). The game labels them as unobserved; they are there to separate real observations from speculation.

### Telescopes

| Telescope | Cost (grants) | Max zoom |
|-----------|---------------|----------|
| Refractor Telescope | free | 15x |
| Observatory Dome | 100 | 150x |
| Orbital Array | 300 | 900x |
| James Webb Class | 700 | 4,500x |
| Tachyon Interferometer | 1,800 | 15,000x |

### Sensors

Visible light is free. Radio, Infrared, X-ray, Ultraviolet and Quantum sensors unlock as you make discoveries and are bought as packs with grants.

### Earning grants

- first discovery of each object
- a **+25% survey bonus** for completing a sector
- **follow-up observations** (+10% of an object's value, once every 2 minutes per object, with the right sensor)
- correct quiz answers (+10 each)
- completing a constellation in the Sky guide (+50)

## Play it

Pick **Pocket Astronomy** on the Little Pause Arcade home page, or open `games/pocket-astronomy/index.html` directly. It is one self-contained HTML file with no build step.

> Browsers only start audio after your first tap or click, so the music begins on first interaction.

## Tech notes

- Plain HTML, CSS and JavaScript in a single file. No frameworks, no build step, no backend.
- Rendering uses the HTML5 Canvas; sound uses the Web Audio API (generated live, no audio files).
- Progress is stored in `localStorage` (keys `pocketAstronomyEdu` and `paSound`).
- Fonts (Fraunces and Hanken Grotesk) load from Google Fonts with system-font fallbacks, so the game still works offline.
- Works in current versions of Chrome, Edge, Firefox and Safari, on desktop and mobile.

## About the data

Values for planets, moons and stars are rounded and meant for learning, not research. Some change over time (for example Hubble's decaying orbit and Voyager 1's distance, which were checked against NASA and news sources in October 2026), and some are uncertain by nature (UY Scuti's size and distance, and star distances in general vary between catalogues). Which sensor reveals each object is a gameplay choice and is not strict physics. If you spot a number that looks wrong, please open an issue.

## Resetting or moving your progress

Use the **Terminal Backup** card to copy your save to text and paste it into another browser or device. The reset button wipes all progress after asking for confirmation.

## License

Add your license here (for example MIT).
