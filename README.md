# VOID RUN: OUTBREAK

A single-file browser survival-horror game exported from a Claude Artifact.

## Run locally

1. Keep `index.html` in the project root.
2. Open `index.html` in a modern browser, or serve the directory with a local static server.
3. The game loads Phaser 3.80.1 from cdnjs, so an internet connection is required when the Phaser library is not cached.

## Deploy to Vercel (static HTML)

1. Create a new GitHub repository named `void-run-outbreak` (public or private as preferred). Do not initialize it with another README if you plan to upload these files directly.
2. Upload `index.html`, `README.md`, and `.gitignore` to the repository root, then commit the changes to `main`.
3. In Vercel, choose **Add New → Project** and import `void-run-outbreak` from GitHub.
4. Set **Framework Preset** to **Other**.
5. Leave **Build Command** blank (no build step is needed for these static files).
6. Leave **Output Directory** as `.` / project root. Do not set it to `dist` or `.next`.
7. Deploy, then open the generated URL and test the game.

No Render service or environment variables are required by this exported HTML file. Phaser itself is loaded from the external cdnjs CDN by the script tag in `index.html`.

## Important scope note

This export is a single HTML artifact with inline JavaScript and procedurally generated textures/audio. It is not a full editable Phaser + TypeScript + Vite source project. The exported HTML's authoring report also said the build had not been played or tested yet, so verify movement, objective progression, enemy behavior, victory/game-over, restart, and browser compatibility before describing it as fully tested.
