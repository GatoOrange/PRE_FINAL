# AGENTS.md — genially_slide

## Project
Single-file HTML presentation (12 slides) for a chemical engineering project. No build system, no package.json, no dependencies beyond CDN fonts/icons. All code in `index.html` (3481 lines: HTML + CSS + JS). No test/lint/typecheck commands exist.

## Run
Open `index.html` directly. For local image serving, use a server:
```bash
python -m http.server 8000   # or: npx serve .
```

## Key facts an agent would otherwise miss
- **`zoom: 1.08` on `body` (line 51)** — affects all sizing; adjust if layout breaks.
- **CSS theming** — edit `:root` vars (lines 12–37) for colors, spacing, shadows. Dark theme: `#121212` bg, `#39b54a` accent, `#e0e0e0` text.
- **Responsive split**: `≤900px` (3-col → 1-col, decorations hidden), `≤600px` (2-col → 1-col, smaller type).
- **All JS is vanilla**, in a single `<script>` block at end of body (lines 3155–3479). No modules, no imports, no build step.
- **Slide engine**: horizontal `translateX` on `.presentation`. 12 `<!-- SLIDE N -->` sections. Add a slide: duplicate `.slide` block, update `data-index`, add dot/label in JS `init()` (lines 3355–3375).
- **Modal system**: `.modal-overlay.show` toggles visibility. `openModal('id')` / `closeModal(event,'id')`. Each modal is a separate block at end of file.
- **Phase step managers**: Fase1 (4 steps), Fase2 (3 steps), Fase3 (6 steps) — each with its own `goToStep*` / `prevStep*` / `nextStep*` functions.
- **`cloneDecorations()`** copies cover slide particles/hexes to all slides. Watermark `"GRUPO 3"` added dynamically.
- **`onerror="this.style.display='none'"`** on logo images — handles missing files gracefully (no broken icons).
- **Media upload** uses `FileReader` + Object URLs, no sanitization — local-only, not production-safe.
- **Font Awesome** (6.5.0) and **Google Fonts (Inter)** require CDN access (internet).
- **`switchModalTab(btn, tabId)`** drives tabbed modals (P&ID, Balance, Industrial).
