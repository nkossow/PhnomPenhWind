# Urban Climate Map Phnom Penh — Animated Wind Flow

Interactive visualization of wind flow patterns over the Urban Climate Map of Phnom Penh (2022), based on data from the [Build4People Project](https://www.build4people.org/) (WP5 Urban Climate).

## Live Demo

Open `wind_animation_v4.html` in any modern browser — no server or dependencies required.

## What it shows

Animated wind particles flow across the urban climate map, following the wind directions measured by Automatic Weather Stations (AWS). The visualization combines two data sources:

- **Base map**: Urban Climate Map Phnom Penh 2022 (INKEK/FONA), showing climatopes from strong cooling potential (light blue) to strong heat load (pink/red)
- **Wind field**: Interpolated from ~90 directional samples taken from AWS wind measurements, using Inverse Distance Weighting (IDW)

### Wind patterns

The dominant pattern is a SW monsoon flow with regional variations:

- **NW sector**: E to ENE flow, strong and dense
- **West/Center**: NE flow, medium intensity
- **South**: N to NNE flow, converging toward the city center
- **Along rivers** (Tonle Sap & Mekong): Channeled and intensified flow
- **River confluence** (W-NW of FFI): Local N-NW vortex around the peninsula
- **Heat island center**: Weak, turbulent flow with thermal mixing

### Weather stations

Seven AWS locations are marked on the map: AUPP, TKK, RUPP1, RUPP2, FFI, DKA, and BPH.

## Controls

| Control | Function |
|---------|----------|
| Speed | Adjusts particle movement speed (0.2×–3×) |
| Particles | Number of animated particles (300–3000) |
| Opacity | Transparency of the particle layer |

## Technical details

- Single self-contained HTML file (~320 KB), no external dependencies
- Base map embedded as Base64 JPEG
- Wind field computed via IDW interpolation of sampled vectors
- Particle system rendered on HTML5 Canvas with `requestAnimationFrame`
- Retina/HiDPI display support via `devicePixelRatio`

## Data sources

- Urban Climate Map: INKEK — Institute for Climate and Energy Concepts, commissioned by the German Federal Ministry of Research, Technology and Space (FONA), January 2023
- Wind measurements: Build4People Project, WP5 Urban Climate, Automatic Weather Stations

## License

Map data and climate analysis © Build4People Project / INKEK. This visualization is provided for research and educational purposes.
