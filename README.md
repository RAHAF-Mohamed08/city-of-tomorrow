# City of Tomorrow — Interactive UAE Smart City Designer

An interactive 3D smart-city design simulator. Pick a UAE reference location (Ajman, Dubai, Abu Dhabi, Sharjah or Fujairah) and design a futuristic, sustainable version of a city: place buildings, trees, parks and roads, then see how your design scores on simple sustainability indicators.

Built as a portfolio project in Data Science and Artificial Intelligence.

**Live demo:** `https://YOUR-USERNAME.github.io/city-of-tomorrow`

<!-- Add screenshots here: ![City of Tomorrow](screenshot.png) -->

## Features

- **3D city workspace** (Three.js): orbit, zoom, pan, rotate buttons, auto-rotate, home view
- **Buildings:** residential, skyscraper, school, hospital, office, with adjustable floors, width, depth, style (box, stepped, tapered, round), material, color, rooftop gardens and solar panels
- **Nature:** single trees (Ghaf and palm), tree groves, lawn and water-saving (xeriscape) parks
- **Infrastructure:** roads, sidewalks, bike lanes, public transport routes, plazas
- **Editing:** select, drag to move, edit in the inspector, rotate, delete
- **History:** undo (button or `Ctrl/Cmd + Z`), reset city
- **Save and load** designs in the browser (localStorage)
- **Sustainability panel** with a score and an explanation of how it is calculated
- **Urban heat view:** an illustrative layer only
- **Responsive:** desktop, tablet and mobile

## Controls

| Action | How |
|---|---|
| Orbit | Left-drag on empty space |
| Pan | Right-drag (two fingers on touch) |
| Zoom | Scroll or pinch, or the `+` / `−` buttons |
| Place an object | Choose a tool, then click the ground |
| Move an object | Select tool, then drag the object |
| Delete | `Delete` key, the Delete tool, or the inspector button |
| Undo | `Ctrl/Cmd + Z` or the Undo button |
| Back to Select | `Esc` |

## How the sustainability score works

The score is a simple number calculated from the objects in your own design. It is **not** a scientific measurement.

| Category | Points | Max |
|---|---|---|
| Green space | 1.5 per tree + 6 per park + 4 per green roof | 35 |
| Solar energy | 5 per building with solar panels | 25 |
| Mobility | 5 per bike lane or transit route + 2 per sidewalk or plaza | 25 |
| Water-saving | 7.5 per xeriscape park | 15 |

The urban heat view is an illustration: buildings and roads warm nearby areas, trees and parks cool them. It does not model real temperatures.

## Real data vs. your design

The design grid is anchored to a real coordinate (the selected city), where 1 grid cell = 10 m, and the status bar shows the approximate coordinates under your cursor. Everything you place is a **proposed design**. The starter buildings are sample objects, not real buildings.

## Run locally

No build step is needed. The app is a single HTML file.

```bash
git clone https://github.com/YOUR-USERNAME/city-of-tomorrow.git
cd city-of-tomorrow
python3 -m http.server 8000
```

Then open `http://localhost:8000`. Opening `index.html` directly in a browser also works. An internet connection is required to load Three.js and fonts from CDNs.

## Deploy with GitHub Pages

1. Rename the file to `index.html` and push it to the `main` branch.
2. Go to **Settings → Pages**.
3. Choose branch `main` and folder `/ (root)`, then save.

## Tech stack

- [Three.js](https://threejs.org/) r128 and OrbitControls
- Vanilla JavaScript, HTML and CSS
- Google Fonts: Caveat and DM Sans

## Roadmap

- [x] **Stage 1:** 3D city with placement, selection, editing, deletion, trees, parks and roads
- [ ] **Stage 2:** Real UAE map (Leaflet + OpenStreetMap) with location search and area selection
- [ ] **Stage 3:** Import real building footprints and roads (Overpass API)
- [ ] **Stage 4:** Richer sustainability indicators and environmental visualizations
- [ ] **Stage 5:** AI design recommendations (greener layouts, tree and park placement, layout comparison). **Coming soon:** no AI service is connected yet.

## Credits and licenses

- Map data (when added in Stage 2–3): © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), ODbL
- Three.js: MIT License
- Fonts: SIL Open Font License

## License

Choose a license for your code (for example MIT) and add a `LICENSE` file.
