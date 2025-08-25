# Interactive Web Apps

Small, self-contained HTML pages for teaching concepts (electronics / data / animation) that can be opened directly or embedded in LMS slides, markdown docs, or presentations.

## Pages

| Page | Purpose | Notes |
|------|---------|-------|
| `pages/potentiometer-divider.html` | Potentiometer voltage divider visualization (dial + vertical schematic) adjustable Vcc, total resistance, wiper position & ADC bits | No query params (direct interaction) |
| `pages/demo-chart.html` | Streaming Chart.js example showing dynamic data updates | Adjustable interval & noise |
| `pages/animation.html` | Simple CSS/JS animation with adjustable speed & size | Pure CSS + small JS |

## Quick Start (Locally)

```bash
git clone https://github.com/rayus86/web_apps
cd web_apps
python -m http.server 8000
# open http://localhost:8000
```

Plain HTML/CSS/JS — no build step.

## Embedding

Example iframe (adjust width/height as needed):

```html
<iframe
  src="https://rayus86.github.io/web_apps/pages/potentiometer-divider.html"
  width="720"
  height="520"
  style="border:0;max-width:100%;background:#0f172a">
</iframe>
```

Same idea for the other pages (demo-chart.html, animation.html).

## Potentiometer Divider Page

Illustrates:
- Relationship between wiper position and segment resistances (R_Vcc & R_GND).
- Output voltage: Vout = Vin * (wiper fraction from GND side).
- ADC reading mapping (0 .. 2^n - 1) based on chosen resolution.

Visuals:
- Circular dial split into two arcs (colored for each resistance segment).
- Vertical schematic with a moving wiper contact.

Possible future enhancements:
- Optional query parameters for preset state.
- Noise / quantization visualization overlay.
- Auto-resizing messaging for host pages.

## Ideas Backlog

- RC filter step response & approximate Bode plot
- Fourier additive synthesis visualizer
- Simple FIR/IIR filter playground
- Theme (dark/light) toggle
- Manifest-driven index auto-generation

## License

MIT (see [LICENSE](./LICENSE)).

© 2025 rayus86
