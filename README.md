# Wind and Sea Watch

Weather, detailed wind and sea state for any location, in one page.

## Open it

**https://mtrehornet.github.io/wind-sea/**

That's it. Nothing to install, no account, no API key. It works in any modern browser on a phone, tablet or computer. Bookmark it or use your browser's **Add to Home screen** to keep it handy.

## How to use it

1. **Search for a place** in the box at the top and press **Search**.
   - A town or beach: `Tybee Island`
   - With a state or country to narrow it: `Ventura, CA` or `Brighton, UK`
   - Exact coordinates, e.g. a spot offshore: `32.0, -80.8`
2. If several places match, **pick one** from the list.
3. Switch **units** with the buttons at the top right:
   - Wind: kn, mph, km/h, m/s
   - Temperature: °F or °C
   - Waves: ft or m

Your last location and units are remembered in your browser for next time.

## What you'll see

- **Now:** temperature, feels-like, humidity, dew point, pressure, cloud cover, visibility, rain chance, sunrise and sunset.
- **Wind:** compass showing where the wind is coming from, sustained speed, gusts, Beaufort force, gust factor, wind at 80 m and 120 m, and the strongest gust in the next 12 hours.
- **Sea state** (coastal and offshore locations only): an animated cross-section of the sea surface built from the forecast swell and wind waves, combined wave height and period, Douglas sea state, primary and secondary swell, wind waves, water temperature and current.
- **48-hour charts:** wind and gusts with direction arrows, wave heights and period, temperature and rain chance.
- **7-day table:** conditions, high/low, rain chance, max wind and gusts, and max waves.

Directions are where the wind or waves are **coming from**. Chart arrows point downwind.

If a place shows "No marine data here", it's inland. Try a nearby beach town or coordinates over the water.

## Data sources

All data comes from [Open-Meteo](https://open-meteo.com/) (CC BY 4.0), fetched live by your browser:

- **Weather and wind:** Open-Meteo "best match" forecast, blending NOAA HRRR/GFS, ECMWF IFS, DWD ICON and other models.
- **Waves and sea state:** Open-Meteo Marine API, using ECMWF WAM, NOAA GFS-Wave and Météo-France MFWAM.
- **Place search:** Open-Meteo Geocoding (GeoNames).

**Not for navigation.** Always check official marine forecasts (NOAA/NWS or your local met office) before heading out on the water.

## Run your own copy

The whole app is one file, `index.html`.

- **On your computer:** download `index.html` and double-click it to open it in your browser.
- **On your own site:** upload `index.html` to any web host.
- **In Home Assistant:** put it in `/config/www/`, open `http://<your-HA>:8123/local/index.html`, and add it to the sidebar with **Settings → Dashboards → Add dashboard → Webpage**.
