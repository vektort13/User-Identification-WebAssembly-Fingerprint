# Vektor T13 - Web Assembly Browser Fingerprint

**Vektor T13 Technologies** • **detect.expert**  
Developed by **Dmytro Momot**

Single‑file, offline **WebAssembly timing micro‑benchmark** that produces a fingerprint‑like feature vector and a **SHA‑256 hash** based on measurements across the **JS↔Wasm boundary** (including *scripted getter/setter* behavior). Includes a **local enrollment gallery** (localStorage), **identify** mode (cosine similarity + Jensen–Shannon distance), and a **multilingual UI** (RU/EN/ZH‑CN/VI).

## What it does
- Builds a tiny Wasm module at runtime (**no .wasm download**).
- Runs timing micro‑tests:
  - **SG0**: scripted getter (Wasm global read)
  - **SS1 / SS2**: scripted setters (argument adaptation)
  - **JS→Wasm** calls and **Wasm→JS** callback timing
- Normalizes → quantizes → down‑samples the feature vector and computes **SHA‑256**.
- Lets you:
  - **Enroll locally** (store samples in `localStorage`)
  - **Identify** against enrolled samples
  - **Export / Import** the gallery as JSON

## Usage
1. Save the HTML file (e.g. `index.html`).
2. Open it in a modern browser (Chromium/Firefox).
3. Click **Collect fingerprint**.
4. Optionally set a label and click **Enroll locally**.
5. Click **Identify** to compare against your local gallery.

## Notes for stable measurements
- Keep the tab focused (foreground).
- Avoid heavy background CPU/GPU load.
- Compare results under similar power/thermal conditions.

## Privacy & ethics
This demo runs offline and does **not** send any data to a server.  
However, fingerprinting can be used for tracking — use responsibly and comply with applicable laws and platform policies.

## License
No license is included by default — add your preferred LICENSE file if you plan to distribute.
