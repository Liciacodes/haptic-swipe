# Haptic Swipe

A swipe-to-delete list with progressive haptic feedback for mobile web. Built with React, TypeScript, and [web-haptics](https://haptics.lochie.me).

---

## What it does

- Swipe a card left → progressive buzz as you drag, thud on delete
- Release early → light snap-back buzz
- Swipe the last card → warning shake + error buzz, then it deletes anyway
- Empty state → because every good app needs personality

---

## Stack

- React + TypeScript
- Vite
- [web-haptics](https://github.com/lochie/web-haptics) by [@lochieaxon](https://twitter.com/lochieaxon)

---

## Getting started

```bash
npm install
npm run dev
```

Then open on your **phone browser** (haptics require real hardware):

```
http://<your-local-ip>:5173
```

Find your IP with `ipconfig` (Windows) or `ifconfig` (Mac/Linux). Make sure your phone is on the same WiFi.

---

## Haptic patterns

| Interaction | Pattern |
|---|---|
| Dragging | `selection` — ticks faster as you pull |
| Snap back | `light` |
| Delete | `heavy` |
| Last card warning | `error` |
| Restore | `success` |

---

## Project structure

```
src/
├── App.tsx          # List state and layout
├── SwipeCard.tsx    # Swipe logic and haptic triggers
├── index.css        # Base styles
└── main.tsx         # Entry point
```

---

## Credits

Haptics powered by [web-haptics](https://haptics.lochie.me) — supports both iOS and Android.
