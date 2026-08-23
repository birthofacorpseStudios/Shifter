# Drone-Man PWA

Deploy-ready for Vercel + PWABuilder.

## Deploy to Vercel (verto)
1. Push this repo to GitHub
2. Import in Vercel - framework: Other, output: . (static)
3. Deploy - HTTPS required for PWA fullscreen

## PWABuilder
1. Go to https://www.pwabuilder.com
2. Enter your Vercel URL (e.g. https://droneman.vercel.app)
3. Manifest will be detected: `manifest.json` with display: fullscreen
4. Build Android / Windows package - will launch with no browser toolbar because:
   - display: fullscreen
   - start_url: /
   - scope: /
   - icons 192 & 512 maskable
   - service worker caching
   - theme_color black

## Files
- index.html - exact game (studio -> title centered -> difficulty -> game) with chip-fix
- manifest.json - PWA manifest (fullscreen, landscape)
- sw.js - offline cache
- icons/ - 192, 512 maskable icons from studio art
- vercel.json - headers for fullscreen permission

## Test fullscreen trusted
On Android Chrome: Add to Home Screen -> launches without URL bar.
PWABuilder validation should show all checks green.
