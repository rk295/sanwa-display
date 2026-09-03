# Sanwa M17 Scout

A browser-based tool for the [Sanwa M17](https://www.sanwa-rc.com/m17) RC radio transmitter.

**Live: https://rk295.github.io/sanwa-display/**

## Features

### Telemetry Viewer
Drag and drop a `.csv` log file exported from the M17 to visualise:
- Steering & throttle over time (with EPA limits marked)
- RPM over time
- Voltage over time
- Lap times and steering/throttle scatter plot

### Model Decoder
Drag and drop a `model.dat` file from the M17's SD card to inspect all saved model slots:
- Model name, FHSS bind ID
- EPA (endpoint adjustment) per channel
- Expo curves
- Condition codes

A sample telemetry log and model file are included in [`demo/`](demo/) for testing.

## Repo layout

```
index.html          # Combined single-page app (self-contained, no build step)
demo/
  260903152734.csv  # Sample telemetry log
  model.dat         # Sample model file (Fast Fox, AE B6.4, Cougar)
```

## GitHub Pages

The site is deployed automatically from the `master` branch root. No build step required — `index.html` is self-contained with demo data embedded as base64 fallback, and loads the `demo/` files via `fetch` when served over HTTP.
