# Attic Light

A WebGL2 simulation of sunlight falling through a gap in an attic roof, lighting dust that drifts in the air, in one HTML file with no dependencies.

## What it does

- **The beam**: sunlight enters through the roof boards at the top left and crosses the frame to the bottom right. It is rendered as single scattering through hazy air, brighter where the light heads toward you, with faint shadows of the boards inside it and edges that soften with distance.
- **Dust**: about 262,000 specks on desktop (98,000 on phones and smaller devices), simulated on the GPU. Each has a real diameter between 3 and 90 µm. Stokes drag ties it to the moving air and gravity pulls it down, so large flakes settle fast and fine dust hangs for minutes. Small eddies too fine for the air grid jostle each speck, more strongly where the air is moving.
- **Light on dust**: specks glow in the beam's core and fall nearly dark in shadow. Brightness scales with each speck's cross-section, flakes flash as they tumble, and specks away from the focus open into soft blur discs, with only a few drifting close to the lens.
- **Air**: a 3D grid of moving air with 25 cm cells. Sun-warmed air in the beam rises slowly, faint draughts keep the room from going still, and swirls hold their shape as they turn.
- **Your hand**: moving the pointer stirs the air. Pressing and dragging swings a hand through the beam: each swing adds its push to whatever wind is already blowing, pushes dust ahead of it and out of view, and leaves clearer air behind. The wind fades over about 8 seconds, and dust from the rest of the room drifts back in over about a minute.
- **The view**: a close-up on the beam, with no text or controls on screen.

## Run it

Open `index.html` in a browser that supports WebGL 2 with float render targets (current Chrome, Safari, Firefox and Edge).
