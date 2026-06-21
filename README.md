# Erg Score Calculator

A lightweight, single-file web calculator for adjusting indoor rowing ergometer scores by age and body weight. Built for masters rowers who want to compare performances across different ages and sizes.

## What it does

Enter your erg time, age, and body weight and the calculator returns:

- **Unadjusted split** — your raw /500m pace, calculated instantly from time and distance
- **Weight-adjusted score** — normalizes your time using the Concept2 formula, so lighter and heavier rowers can be compared on equal footing
- **Age-adjusted score** — applies the USRowing masters handicap, giving older rowers a time credit relative to a base age of 27
- **Combined adjusted score** — both adjustments applied together, age handicap first then weight factor

Supports 1000m, 2000m, and 5000m with a custom distance option. Body weight can be entered in lbs or kg.

## Formulas

**Age adjustment** — USRowing masters handicap formula for singles (K = 0.025):

```
Handicap (seconds) = (Age − 27)² × 0.025
```

No adjustment applied for ages 27 and below.

**Weight adjustment** — Concept2 standard formula:

```
Adjusted Time = Actual Time × (Body Weight in lbs / 270)^0.222
```

Rowers lighter than 270 lbs receive a faster adjusted time; heavier rowers are slowed proportionally.

## Usage

No build process, no dependencies. Just open `erg-calculator.html` in any browser, or host it anywhere that serves static files.

**GitHub Pages:** Upload to a repository, enable Pages under Settings → Pages, and your calculator will be live at `https://yourusername.github.io/repo-name`.

## Sources

- Age formula: [USRowing Masters Rowing](https://usrowing.org)
- Weight formula: [Concept2 Weight Adjustment Calculator](https://www.concept2.com/training/weight-adjustment-calculator)
