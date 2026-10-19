# Thrilok Chaitanya — Spatial Workspace

A responsive spatial portfolio with a fixed top navigation and FuzzyText system label, draggable desktop panels, a synchronized project directory and inspector, a workspace terminal, contact links, a cursor-reactive MagnetLines background, a custom target cursor for desktop pointers, and a rotating Three.js sphere that pauses when the pointer hits it. Motion effects respect reduced-motion preferences and the page remains usable without WebGL.

MagnetLines uses canvas and TargetCursor uses DOM/CSS, so the portfolio does not need React or OGL dependencies.

The project inspector contains exactly four external projects: DevGuard, VERITY — Evidence Intelligence, Proof Layer, and Network Intrusion Detection System. Project descriptions and links are centralized in `src/config/workspaceConfig.js`. The DevGuard preview is a screenshot of its public site at `public/assets/previews/devguard.png`; projects without a captured screenshot show a labeled preview fallback.

## Run locally

The page uses JavaScript ES modules, so serve the folder over HTTP instead of opening `index.html` directly.

```powershell
cd C:\Users\thril\Projects\portfolio2.0
py -m http.server 4173
```

Then open <http://localhost:4173>. Python 3 must be installed. The Three.js and font assets are loaded from CDNs; the page still works without the 3D background if Three.js or WebGL is unavailable.

## Update profile and projects

Edit `src/config/workspaceConfig.js`. Project descriptions, statuses, verified links, technologies, and preview paths are maintained there. The interface is built in `src/components/SpatialWorkspace.js`, with styles in `src/styles/spatialWorkspace.css`.
