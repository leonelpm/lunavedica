# Luna Védica

A browser-based Vedic astrology birth chart calculator. All calculations run entirely in your browser — no birth data is ever sent to a server.

## Features

- **Rasi (D1) chart** — the main birth chart using the South Indian square grid format.
- **Navamsa (D9) chart** — the divisional chart for deeper insight into relationships and dharma.
- **Planetary positions table** — shows each planet's sign, degree, and house, including Rahu and Ketu.
- **Lahiri ayanamsa** — applies the standard Vedic sidereal correction via Swiss Ephemeris.
- **Auto-geocoding** — type any city name and the app resolves its coordinates via OpenStreetMap Nominatim.
- **Auto timezone** — automatically determines the historical UTC offset for the birth location and date using the IANA timezone database.
- **Bilingual** — full Spanish and English interface.

## Usage

1. Enter the **city of birth**. The app will look up coordinates automatically.
2. Enter the **birth date** in DD/MM/YYYY format.
3. Enter the **local time** of birth.
4. The **time zone (UTC)** and **latitude/longitude** fields are optional — they are filled automatically from the city lookup. Override them manually if needed.
5. Click **Calcular carta / Calculate Chart** to generate the charts.
6. Click **Restablecer / Reset** to clear the form back to its default values.

## Technical Details

| Component | Technology |
|-----------|-----------|
| Ephemeris engine | [Swiss Ephemeris](https://www.astro.com/swisseph/) compiled to WebAssembly via [prolaxu/swisseph-wasm](https://github.com/prolaxu/swisseph-wasm) |
| Geocoding | [OpenStreetMap Nominatim](https://nominatim.openstreetmap.org/) (free, no API key required) |
| Timezone lookup | [timeapi.io](https://timeapi.io/) (free, no API key required) |
| Chart rendering | Pure SVG, South Indian style |
| Frameworks | None — vanilla HTML, CSS, and JavaScript |

## Running Locally

No build step is required. Open `index.html` directly in a browser, or serve it with any static file server:

```bash
npx serve .
# or
python3 -m http.server
```

## License

MIT
