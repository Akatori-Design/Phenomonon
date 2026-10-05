# Rain on Glass

A WebGL2 simulation of rain on a window, in one HTML file with no dependencies.

## What it does

- **Drops** land at random, sag under their own weight, and merge into one drop holding their combined volume when they touch. Heavy drops break free and run down as one U-shaped body, losing water as they go, and small ones come to rest when they run out.
- **Refraction**: every drop and stream acts as a small lens showing an inverted view of the street, with dark rims and soft highlights.
- **Condensation** fogs the glass; running water clears channels through it, and it slowly forms back.
- **Streams** pour from the top of the pane only above 70% rainfall; at any rainfall, a running drop that gathers enough water opens a stream of its own. Streams meander down, carry surges of water, merge with each other, absorb drops they touch, and thin out and dry when no more water reaches them.
- **Wiping**: drag to wipe as if with three fingers. The fingertips wipe clean while the lower fingers only smear; the fingers tilt with the arm. Pushed water collects in a strip in front of the fingers and breaks into drops when you lift. Holding your fingers still makes water flow around them.
- **Wipe lines** hold water back: drops spread along the line until they break through, and streams pool at the edge, then fall straight down. The resistance fades as the glass fogs over.
- **Splashes**: the heavier the rain, the harder drops hit. A hard hit shatters the instant it lands into a smaller centre and a radial ring of beads; the jolt shakes nearby drops and can knock loose ones that were close to sliding.
- **Sound** (starts on your first click; toggle in the panel): a deep knock for each drop that lands over a wash of rain, both following how heavy the rain is.

## Controls

Rainfall, drop size, condensation, refraction and fog sliders (50% is the tuned default), a choice of view outside, wipe glass, pause, sound, and "Use a photo" to look through your own image (or drop one onto the page).

## Run it

Open `index.html` in a browser that supports WebGL 2.
