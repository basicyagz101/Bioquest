# Bioquest — Feedback Fixes (November 2026)

Open `index.html` in a modern browser. All required files are relative and work offline (except organization links and external web fonts).

## Contents
- `index.html` — the original website sections, plus Opportunities Map side panel and legend
- `style.css` — accessible responsive layouts and five-color visual theme
- `script.js` — game, original five quizzes, Team Builder, offline interactive county map
- `assets/` — replaceable pixel-art background, sprites, font, and audio

## Updates from peer-testing feedback
1. Game walkways now enforce map edges, solid building/fountain/water boundaries, and collision with structures. Movement is axis-separated to permit sliding along obstacles. The `CAMPUS_ROUTES`, `CAMPUS_OBSTACLES`, and `CAMPUS_LOCATIONS` arrays at the top of the campus code in `script.js` are editable when new art is provided.
2. Team HQ and Main Research Center display interaction dialogue when the player stands at their marked entrances and presses E. Five sector lab entrances still open the existing Team Builder and quizzes.
3. Map displays clickable, keyboard-accessible shapes for all 21 NJ counties; hover highlights boundaries and clicking opens the county's opportunities in the adjacent panel. Counts inside counties replace cryptic letter markers.
4. Filter selections use **AND** (a record must match every selected option). Because each data record has one type, one sector and one county, selecting two types may correctly produce zero results.
5. Career pathway steps on the quiz result page are now interactive. Original quiz scenarios and role scoring are unchanged.
6. Visual polish improves layout, map readability, reuse of the pixel campus illustration, and consistent five-color palette. The background and PNG sprites are recolored but keep stable filenames for replacement.

### Music
Music: **“Local Forecast” by Kevin MacLeod**. Supplied recording at `assets/audio/bioquest-game-map-theme.mp3`. It plays only in Game and Map. Switching between those screens preserves playback position; returning Home pauses and resets. A browser may require a click to begin audio.

### Opportunity data notice
All opportunity records are from the supplied original project and have *not* been live-verified. Check with organizations for availability.

### Art and navigation
Replace `assets/backgrounds/biotech-campus-background.png` to swap campus art. Revisit collision route coordinates in `script.js` if the replacement art has a different layout. Edit `CAMPUS_LOCATIONS` for entrances and `CAMPUS_OBSTACLES` to reflect new building/water locations.

County boundary shapes are embedded in `script.js` for offline operation, derived from the sample US counties shapefile packaged with Basemap (not legal survey boundaries).

## Contributions (user-provided)
- Matthew: game and map
- Leah: style and logo
- Natalie: sprite art
- Aditya: game quizzes and TASKS.md

## Check before presenting
See `TESTING.md` for smoke test instructions, browser behavior, and known limits.

## November follow-up — restored game art and simplified team recruitment
- Added the supplied Bioquest logo to the home splash and both site navigation headers (`assets/bioquest-logo.png`).
- Restored the original colorful campus background and original player sprite from the previously supplied project; the Opportunities Map was not modified.
- Replaced the narrow route-limited movement with polygon building footprints, water margins, a fountain hitbox, and map-edge limits. Door markers have been repositioned to the corresponding building entrances. Collision polygons remain editable in `script.js`.
- Click an occupation to add it directly to your six-person team; click it again to remove it. The previous confirmation popup is gone.
- Collision alignment should still be playtested on the actual browser/device before presenting; no screenshots or assets are required for future adjustments unless artwork changes.

## Home game card visual revert
Restored the original clean controller icon on the Build-A-Biotech Startup home card; removed the campus image texture/overlay from that card. The supplied logo remains untouched in the site header and splash area.

## Latest improvements (Nov 2, 2026)
- Unmodified user-supplied logo is now large on the Home splash and centered in the Home header.
- Campus collision footprints revised to leave wide walkable lanes, with per-axis sliding and small-step motion to avoid tunneling. Source polygons: `CAMPUS_OBSTACLES` in `script.js`.
- Campus title/instructions centered and spaced more carefully.
- Music toggle added to persistent Game/Map navigation. Muting does not restart the track; Game/Map retain one music session and leaving them resets it.
- Removed touchscreen arrow/enter pads from the entry scene and campus. Movement uses keyboard WASD/arrow keys and E for interaction. Mobile users need a keyboard to traverse the campus in this build.
- The Opportunities Map, five quizzes, and team selection data were not modified.


## Marine quiz update
The Marine sector incorporates all five scenarios, four options and 3+1 competency scoring from the provided `marinegame.txt`. It now includes decision feedback, a five-competency results summary, archetype analysis and decision review. The marine assessment is integrated into the existing game and uses the existing Bioquest theme. The other four quizzes and Opportunities Map were not intentionally changed.
