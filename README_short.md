# ⚡ NOAA Lightning Strikes (2009–2018)

A look at 10 years of U.S. lightning data — one dashboard in **Tableau**, and a parallel analysis in **Python** (Plotly + Folium).

I wanted to answer a simple question: *when and where does the U.S. get hit with the most lightning?* Turns out it's almost entirely a summer story.

## What's here

**Tableau dashboard** — a one-page overview with total strikes, peak day, a rolling daily average, a month/week calendar heatmap, and a density map over the U.S. Filterable by year.

**Python (Plotly)** — monthly and yearly bar/line charts breaking down seasonality and the 10-year trend.

**Python (Folium)** — a strike density heatmap over an open-source basemap, as a sanity check against the Tableau map.

## What the data shows

- Lightning is heavily seasonal — **June through August** account for the majority of strikes, with **August the consistent peak** in both the single-year and 10-year views.
- Annual strike counts trended up over the decade, from ~30M (2009) to ~43M+ (2018), with a small dip around 2012.
- Hotspots cluster along the **Gulf Coast and Southeast** — shows up in both the Tableau/Mapbox map and the Folium map, which was a nice cross-check.

## Stack

Tableau · Python · Pandas · Plotly · Folium

## Structure

```
noaa-lightning-strikes/
├── tableau/          # .twbx dashboard
├── python/           # plotly + folium scripts
├── data/             # source CSV
└── assets/           # screenshots
```

## Run it

```bash
pip install pandas plotly folium
python python/monthly_strikes_plotly.py
python python/yearly_trend_plotly.py
python python/density_heatmap_folium.py
```

Open the `.twbx` file in Tableau Desktop or Tableau Public (free) to view the dashboard.

---
Data: NOAA National Centers for Environmental Information.
