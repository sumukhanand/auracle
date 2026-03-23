# Auracle
 
**Turn your hearing test into personalised headphone EQ settings.**
 
Auracle takes audiogram data — the dB thresholds measured at each frequency during a hearing test — and generates an inverse EQ correction curve. The result is a set of parametric or graphic EQ filter settings you can paste directly into your EQ app of choice.
 
---
 
## How it works
 
When you take a hearing test wearing your headphones, the measured thresholds capture both your personal hearing profile *and* the frequency response of those specific headphones in one combined measurement. Inverting this curve and applying it as EQ brings the perceived response closer to neutral for your ears on that specific pair of headphones.
 
The correction is scaled (default 10%) to avoid over-processing — you can increase this to taste.
 
---
 
## Features
 
- **Add any frequency** — use preset buttons (20 Hz–20 kHz) or type a custom value. No fixed grid.
- **EQ curve preview** — live canvas visualisation updates as you enter values.
- **Parametric EQ output** — SoundSource-compatible format with auto-calculated preamp gain.
- **Graphic EQ output** — 5, 10, 15, or 31 band options, sampled from the parametric curve.
- **Normalisation** — subtracts the mean gain across the audible range so net perceived loudness stays neutral. Useful for A/B comparing EQ on/off.
- **Correction scale slider** — scale the entire curve from 10–100% to dial in intensity.
- **One-click copy** — exports ready-to-paste filter settings.
 
---
 
## Usage
 
### Step 1 — Take a hearing test
 
Wear your headphones and take a free hearing test at your normal listening volume:
 
- [hearingtest.online](https://hearingtest.online)
- [mimi.io](https://mimi.io)
 
Note the dB threshold at each frequency. A positive value means you need more volume at that frequency to hear it — Auracle treats these as the correction amount.
 
### Step 2 — Enter your values
 
Enter the dB values into Auracle's frequency grid. Add intermediate frequencies (e.g. 375 Hz between 250 and 500) for higher resolution.
 
### Step 3 — Export and apply
 
**SoundSource (Mac)**
1. Switch to **Parametric** mode
2. Click **Copy**
3. Paste into a `.txt` file, e.g. `Auracle.txt`
4. In SoundSource → Headphone EQ → **Add Other Profile…** → select the file
 
**Wavelet (Android)**
1. Switch to **Graphic EQ** mode, select your band count
2. Copy the band values and enter them manually into Wavelet's equalizer
 
---
 
## EQ chain order
 
If you're also applying a headphone correction profile (e.g. from [AutoEQ](https://autoeq.app) or [oratory1990](https://www.reddit.com/r/oratory1990/wiki/index/headphone_eq_settings/)), apply that **first**, then layer Auracle's hearing correction on top:
 
```
Source → Headphone correction (AutoEQ) → Hearing correction (Auracle) → Ears
```
 
This ensures Auracle is compensating for your hearing alone, not a mix of headphone coloration and hearing differences.
 
---
 
## Tips
 
- **Scale** — start low (10–20%) and increase gradually. Raw audiogram values are large; a full 100% correction can sound unnatural.
- **Per-ear differences** — if your audiogram shows different values per ear, average them, or weight slightly toward the weaker ear.
- **Normalisation** — keep this on when comparing EQ on/off so any perceived difference is tonal, not a volume change.
- **Retake the test** if you switch headphones — the correction is specific to the headphone you wore during the test.
 
---
 
## Stack
 
A single self-contained HTML file — no dependencies, no build step, no backend. Pure HTML, CSS, and vanilla JavaScript.
 
---
 
## Credits
 
Built with [Claude](https://claude.ai) by Anthropic.
 
Headphone EQ methodology informed by the work of [oratory1990](https://www.reddit.com/r/oratory1990) and the [AutoEQ project](https://github.com/jaakkopasanen/AutoEq).
 
SoundSource custom profile format by [Rogue Amoeba](https://rogueamoeba.com/soundsource/).
