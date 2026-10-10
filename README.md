# Malvan Connect

A lightweight, bilingual community companion for Malvan, Sindhudurg. It brings local marine and rain forecasts, travel links, landmark information, market reports, and a neighbourhood board into one responsive page.

## Features

- **Tide & fishing:** Model-based sea-level, wave and current estimates; approximate high/low turns; moon phase; and a lower-wave/current time estimate.
- **Monsoon alerts:** Three-day rain outlook, recent IMD alerts mentioning Malvan/Sindhudurg/Konkan, and community hazard reports for heavy rain, flooding and road closures.
- **Market prices:** Community-entered fish and crop prices for Sindhudurg, Ratnagiri and Raigad.
- **Community board:** Local requests, offers, jobs, lost/found, boat or vehicle hire, and announcements. Posts can include photos and videos.
- **Bus travel:** Route booking links for Mumbai/Pune to Malvan, with operator contacts where publicly listed.
- **Explore Malvan:** A photo gallery of local landmarks with image credits and licenses.
- **English and Marathi:** Switch languages from the header. The rotating Malvan/Konkan slogan ribbon remains visible as you move through the sections.
- **Light and dark themes:** The selected theme is remembered in the browser.

## Run locally

This is a static site with no build step or project dependencies. Serve the folder over localhost so browser APIs and live data requests work:

```sh
npx --yes serve .
```

Open the local URL printed by the command. The page also works with a static-server extension in VS Code.

## Data and privacy

- Tide, wave, current and rain estimates come from [Open-Meteo](https://open-meteo.com/). Coastal marine values have limited accuracy and are **not for navigation or safety decisions**. Check official IMD and local harbour advice before going out.
- Official weather alerts link to [IMD warnings](https://mausam.imd.gov.in/responsive/districtWiseWarningGIS.php) and are read from the [IMD CAP feed](https://cap-sources.s3.amazonaws.com/in-imd-en/rss.xml).
- Market rates, community posts and hazard reports are saved only in the current browser. They are not shared with other users or synced to a server. Confirm community prices before trading.
- Post attachments are stored in this browser using IndexedDB. Each post accepts up to three image/video files, 10 MB per file and 15 MB total.
- Device notifications can show fresh IMD alerts while the page is open. Background push notifications require a shared server, which this static app does not include.
- Slogans are original, locally inspired lines, not historical quotations.

## Project files

- `index.html` — page structure and content
- `styles.css` — responsive layout and light/dark themes
- `app.js` — translations, local storage, forecasts and interactions
- `favicon.svg` — browser tab icon