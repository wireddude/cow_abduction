# Cow Abduction

A family-friendly flying-saucer game for phones, tablets, and desktop. Pilot a shiny 1950s flying disc over one moonlit farm and lift cows and neighbors aboard with a tractor beam.

This is a first playable version. There is one farm, the visitors only wander, and there is no combat. Enemies and strategy are intentionally left open.

## Play

The game is the `index.html` file in this folder, so a GitHub Pages site pointed at the repo root can serve it. This project does not change any repository settings.

Open it through a local web server. Module scripts do not run from a `file://` address.

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`.

On an iPhone or iPad, open that address in Safari. The on-screen pad and BEAM button are sized for thumbs, and the page uses the full screen including the safe areas.

## How to play

- Fly with the pad on the lower left, or with WASD / the arrow keys.
- Hold the BEAM button, or hold Space or B. Cows and people inside the ring float up, wriggle, and pop into the saucer. The score counts cows and people separately.
- Let go before they reach the ship and they drift back down, unharmed.
- Restart with the Restart button or the R key. Pause with Pause, Esc, or P.
- Sound is optional. It starts after the first tap or key press. SOUND ON / SOUND OFF remembers your choice.

When everyone is aboard, the night ends. Play again to bring the farm back.

## In this version

- One night farm: fields, a dirt track, a barn, a farmhouse, a silo, fences, a pond, trees, and a garden.
- A silver flying disc with a dome and rim lights. It hovers, it does not fight.
- Cows and people wander their parts of the farm. They do not chase, dodge, or attack.

## Extending

Everything for the game lives in `index.html`.

- `COW_VARIANTS` and `COW_SPOTS` add cows.
- `PEOPLE` and `PEOPLE_SPOTS` add neighbors. Outfits are plain clothing, hats, and colors.
- `buildFarm()` is the level.
- `window.__cowAbduction` can `start()`, `place(x, z)`, `setBeam(true)`, and `state()` while you are trying a change.

Keep new visitors as wanderers until there is a real design for anything else. Do not bolt on weapons or enemy behavior in this loop.
