# Wind and Sea Watch

Weather, detailed wind and sea state for any location, in one page.

## Open it

**https://mtrehornet.github.io/wind-sea/**

That's it. Nothing to install, no account, no API key. It works in any modern browser on a phone, tablet or computer. Bookmark it or use your browser's **Add to Home screen** to keep it handy.

## How to use it

1. **Pick a place.** Either:
   - Tap the **target button** next to Search to use your current location. Your browser will ask permission the first time. Location is only read when you tap the button.
   - Or type in the box and press **Search**:
     - A town or beach: `Tybee Island`
     - With a state or country to narrow it: `Ventura, CA` or `Brighton, UK`
     - Exact coordinates, e.g. a spot offshore: `32.0, -80.8`
2. If several places match, **pick one** from the list.
3. Switch **units** with the buttons at the top right:
   - Wind: kn, mph, km/h, m/s
   - Temperature: °F or °C
   - Waves: ft or m

Your last location, units and boat choice are remembered in your browser for next time.

## What you'll see

- **Conditions:** temperature, feels-like, humidity, dew point, pressure, cloud cover, visibility, rain chance, sunrise and sunset.
- **Wind:** compass showing where the wind is coming from, sustained speed, gusts, Beaufort force, gust factor, wind at 80 m and 120 m, and peak gusts for the next 12 hours and last 24 hours.
- **Sea state** (coastal and offshore locations only):
  - An animated cross-section of the sea surface built from the forecast swell and wind waves.
  - **Time slider:** drag to see the sea from 24 hours ago to about 7 days ahead, press play to watch it change, or press **Now** to jump back.
  - **Boat:** choose a buoy, kayak, center console, sailboat, sportfisher or motor yacht. Each is drawn to scale and rides the waves, so you can see how its length compares with the distance between wave crests.
  - Wave heights are exaggerated up to 4× so they're easy to see. Tick **True scale** for real proportions.
  - Combined wave height and period, Douglas sea state, primary and secondary swell, wind waves, wind, water temperature and current for the selected hour.
- **Charts for the past 24 hours and next 48 hours:** wind and gusts with direction arrows, wave heights and period, temperature and rain chance. The past is shaded and an orange **NOW** line marks the present. When you move the time slider, a dashed line shows that hour on every chart.
- **Daily table:** yesterday (greyed), today (highlighted) and the next 6 days, with conditions, high/low, rain chance, max wind and gusts, and max waves.

Directions are where the wind or waves are **coming from**. Chart arrows point downwind.

If a place shows "No marine data here", it's inland. Try a nearby beach town or coordinates over the water.

## Data sources

All data is fetched live by your browser:

- **Weather and wind:** [Open-Meteo](https://open-meteo.com/) (CC BY 4.0) "best match" forecast, blending NOAA HRRR/GFS, ECMWF IFS, DWD ICON and other models.
- **Waves and sea state:** Open-Meteo Marine API, using ECMWF WAM, NOAA GFS-Wave and Météo-France MFWAM.
- **Place search:** Open-Meteo Geocoding (GeoNames).
- **Name of your current location:** [BigDataCloud](https://www.bigdatacloud.com/) free reverse geocoding (only when you tap the location button).

History is recent model data, not station observations. Boats simply follow the water surface; real boat motion depends on hull, speed and heading.

**Not for navigation.** Always check official marine forecasts (NOAA/NWS or your local met office) before heading out on the water.

## Run your own copy

The whole app is one file, `index.html`.

- **On your computer:** download `index.html` and double-click it to open it in your browser.
- **On your own site:** upload `index.html` to any web host. The location button needs an `https://` address.
- **In Home Assistant:** put it in `/config/www/` and add a dashboard with a panel view containing a Webpage (iframe) card pointing to `/local/index.html`, with `allow: "fullscreen; geolocation"`. On a plain `http://` address, the location button falls back to your Home Assistant person location.
