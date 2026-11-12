# KISS & FIGHT: LOVE IS WAR

A 2D arcade fighting game (Ky vs Chea) in a single dependency-free HTML file.

## Run locally
Open `index.html` in any modern browser (double-click it), or serve the folder:

    npx serve .
    # or
    python3 -m http.server 8080   # then open http://localhost:8080

## Controls
P1 keyboard: A/D move, W jump, J punch, K heavy punch, L kick, U heavy kick, I kiss, S block, Shift dodge
P2 keyboard: Arrows move, Z/X/C/V attacks, B kiss, N dodge
Gamepad (P1): stick/d-pad move, A jump, X/Y/B/RT attacks, RB kiss, LB block, LT dodge
Mobile: on-screen buttons (landscape). Esc pauses.

## Deploy to the web
Upload `index.html` to any static host (Netlify Drop, Vercel, GitHub Pages, Cloudflare Pages). No build step.

## Package for mobile later
Wrap the folder with Capacitor:

    npm init -y && npm i @capacitor/core @capacitor/cli
    npx cap init kissfight com.example.kissfight --web-dir=.
    npx cap add android && npx cap add ios
    npx cap sync

## Code layout (inside index.html)
Sections: AUDIO, INPUT, DATA, FX, COMBAT, AI, ROUNDS, DRAW, MENUS, LOOP.
