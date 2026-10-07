# Phenomenon

A collection of interactive animations of natural phenomena, each built as a single self-contained web page.

## Projects

| Project | What it is |
| --- | --- |
| [Rain on Glass](rain-on-glass/) | Rain running down a fogged window: drops that land, merge, drip and refract the street behind, streams in heavy rain, and glass you can wipe with three fingers. |
| [Attic Light](attic-light/) | Sunlight through a gap in an attic roof: dust drifting in the beam, glowing where the light catches it, that you can stir and sweep away with the pointer. |

## Running a project

Each project is a folder with an `index.html`. Open it in a current browser, or serve the repo locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/<project-folder>/`.

## Packages

Projects can also ship as private, installable web components on GitHub Packages. Only the
minified build, the licence and a README are published; the readable source stays here.

| Package | Element | Source page |
| --- | --- | --- |
| [`@akatori-design/rain-on-glass`](packages/rain-on-glass/) | `<rain-on-glass>` | [rain-on-glass/index.html](rain-on-glass/index.html) |

Each package is generated from its project's `index.html`, so keep editing the page, then rebuild:

```bash
cd packages/<project-folder>
npm install
npm run build
```

Open `packages/<project-folder>/demo.html` through the local server above to check the element.
`npm pack --dry-run` shows exactly which files would be published. Install and usage steps for
people using a package are in that package's own README.

Every package is signed **Hiro · Akatori Design**: a copyright notice at the top of the built
file, a credits comment inside the element, a `credits` property, and a credit line in the
control tray. Each is under a proprietary licence; see the package's `LICENSE`.

### Adding a package for another project

1. In the project's `index.html`, route every `window` and `document` access through a
   `// ---------- host ----------` block at the top of the script, as `rain-on-glass` does.
2. Copy `packages/rain-on-glass/` to `packages/<project-folder>/` and adapt `build.mjs`, the
   element's attributes, `package.json`, `LICENSE`, `README.md` and `demo.html`.
3. Build, check the demo, and run `npm pack --dry-run` before publishing with `npm publish`.
   Publishing needs a GitHub token with the `write:packages` scope.
