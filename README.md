# a-journey-back-to-marsa-al-arab

# A Journey Back to Marsa Al Arab

An interactive, single-file 3D prototype that lets you revisit a real place through the memories that happened there — instead of watching a sightseeing tour, you step ashore at Marsa Al Arab and walk to the exact spots where three photos were taken.

This is a concept demo for a broader idea: **spatial memory journeys** — turning a group's routes, photos, videos and voice notes into one explorable world, positioned by both place and time.

<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/0d7633f9-5d2f-44de-8e97-8ee1fa4cfa60" />
<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/3fa2670a-c89f-4d18-ac52-53f067fac7e1" />
<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/af44d5b1-db47-4968-b5e5-c49d751aaf6b" />
<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/3410b9a7-4c46-4a9f-9656-03cc522dde9d" />
<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/4903e90e-46a4-4985-bc57-dfdb68d5edc4" />
<img width="1397" height="659" alt="image" src="https://github.com/user-attachments/assets/8b3cc3dc-a9ea-4b48-9fbd-82e27665202b" />


## What it is

- A yacht arrives at Marsa Al Arab Marina and docks.
- You step ashore and freely walk the promenade (WASD / arrows, drag to look, on-screen joystick on mobile).
- Three photo memories are hidden along the route. Walk up to one and a prompt lets you open it.
- The Navigator (bottom sheet) shows a schematic map of the district, your position, and which memories you've found — tap one to get guided toward it.
- Once all memories are found (or you choose to leave early), you walk back, board the yacht, and watch it drift out to open water.
- The journey ends on a "Concept preview" screen: three short pitches (a group trip, a wedding, a major sporting event) showing what this idea could become, plus a **Restart this journey** button.

## Status

This is an early, single-scene prototype — not a finished product. A few quiet in-experience notes call this out directly:

- The 3D environment is placeholder geometry; the final version is intended to use photorealistic reconstructions of the real location.
- Photo-to-viewpoint alignment (matching each memory's photo to the exact camera angle in the 3D scene) is a work in progress.

These notes are intentionally understated — small text, no icons, no interruption to walking or looking around — and each only appears once per journey.

## Tech

- **Single HTML file** — no build step, no dependencies to install. Open it in a browser and it runs.
- **[Three.js](https://threejs.org/)** (r128) for the 3D scene, camera, and rendering, loaded from a CDN.
- Procedural geometry, lighting, and simple audio synthesis — no external 3D assets or model files.
- Vanilla JS for all state management, walking/collision, the memory system, the Navigator map, and UI.
- Responsive layout: desktop, and mobile in both portrait and landscape.
- Respects `prefers-reduced-motion` for fades and transitions.

## Running it

No build tools, no server required for local viewing:

1. Download `dubai-marsa-journey.html`.
2. Open it directly in a modern desktop or mobile browser.

(Serving it over a local static server, e.g. `python3 -m http.server`, avoids any browser restrictions on local file access and is recommended if audio or fonts behave oddly when opened directly from disk.)

## Project structure

This repo is intentionally minimal:

```
dubai-marsa-journey.html   # the entire experience — markup, styles, and logic in one file
```

Everything — the 3D scene setup, the yacht arrival/docking sequence, the walkable district, the memory system, the Navigator map, and the ending screen — lives in this single file to keep the prototype easy to share, fork, and iterate on without a build pipeline.

## Roadmap / concept direction

This prototype is a proof of concept for a larger idea. Where it could go next:

- Photorealistic environment reconstruction of the real location (replacing the current procedural geometry).
- Precise photo-to-viewpoint alignment, so a memory's photo lines up with the exact spot and angle it was taken from.
- Support for video and audio memories, not just photos.
- A real timeline view — positioning memories by *when* they happened as well as *where*.
- Multi-person journeys: everyone's routes and memories woven into one explorable world (a trip, a wedding, a sports event).

## License

TBD — add a license before making this repository public if you intend others to reuse or contribute to it.
