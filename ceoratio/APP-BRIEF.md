# CEO Ratio — Build Brief (Ground Truths series, app #2)

Decided by Bryan 10/11–10/13/26. Same play as GroundTruth, start to finish.

## Identity
- Series: **Ground Truths**
- App: **CEO Ratio** (launcher name)
- Android Studio project: `CeoRatio`
- Package: `com.afnuke.ceoratio`
- Credit line: © 2026 Afnuke / AI collaboration

## The rule: same everything, different statistics
Clone GroundTruth's engine, card design, boot, flow, signing, and pipeline.
A person who finds one app finds the other — each catches users for the other.
Only two things change:
1. **The statistics** — CEO pay ratio data instead of profit per worker.
2. **The background** — same number-rain system, but **gold**, and what falls is the
   real CEO pay figures. (Green = the workers' money. Gold = the boss's.)

## The card (on detection, same as GroundTruth)
- CEO's real face (photo) next to the numbers — the reveal happens in the app.
- Big figure: the ratio, e.g. **6,666:1**
- Line under it, exact pattern: "He makes 6,666 times what each of his workers makes — and he has 2,000,000 of them."
  (Ratio and headcount REAL per company, always. Wording pattern approved by Bryan 10/11.)
- CEO name, CEO pay, median worker pay, total headcount.
- Company with no verified disclosure (7 of 74): card shows "Not disclosed" — never a guessed number.

## Data (ready — drag-and-drop, no pasting)
- `CeoData.kt` in this folder: all **74 companies**, data class + `ceoRatioBank` list.
  67 with verified FY2024 ratios (company-stated, DEF 14A Item 402(u)); 7 null with reasons.
  Source research: `ceo-pay-ratios-fy2024.md` (same folder).
- **Headcount** is not in CeoData.kt — Gemini merges it from GroundTruth's seed data by ticker.
- **Known gap — CEO photos:** CeoData.kt carries `photoSource` (the source PAGE, not an image file).
  Real image files must be gathered with license care before the face ships in the app.
  Until then the card uses a silhouette with a question mark (same as the pitch videos).

## Pipeline (mirror GroundTruth exactly)
1. Duplicate the GroundTruth project as `CeoRatio`; change package + label.
2. Drop `CeoData.kt` into the project; wire the card to the ratio data; gold rain.
3. Git init + commits at each step (Bryan never touches git himself — Gemini reports hashes).
4. Release signing with a keystore, same as GroundTruth.
5. GitHub repo `afnuke/ceoratio` + release, same pattern as `afnuke/groundtruth`.
6. Build signed AAB + release APK; test on the Pixel (lab) and Motorola (legs).
7. Play Console: new app listing, declarations, privacy policy page (GitHub Pages, mirror
   `afnuke/groundtruth-privacy`), closed testing alpha track.
