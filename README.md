# Tallinn Weather Forecast

A 30-day weather forecast app for Tallinn with both CLI and web interfaces. Real weather data for the first 16 days from Open-Meteo API, extended with realistic forecast data to 30 days.

## Features

- 🌦️ **Real Weather Data** - Uses free Open-Meteo API (no auth required)
- 📊 **30-Day Forecast** - 16 days actual + 14 days extrapolated
- 🖥️ **CLI Interface** - Terminal-based display with formatted tables
- 🌐 **Web Interface** - Beautiful responsive card layout
- 📈 **Statistics Dashboard** - High/low temps, averages, total precipitation
- ♨️ **Caching** - 1-hour browser cache to reduce API calls

## Quick Start

### CLI

```bash
npm install
npm run dev
```

### Web Interface

Simply open `index.html` in your browser or serve it locally:

```bash
npx http-server .
```

Then open `http://localhost:8080/index.html`

## Project Structure

```
├── src/
│   └── index.ts          # CLI weather app
├── index.html            # Web interface
├── package.json          # Dependencies
├── tsconfig.json         # TypeScript config
└── README.md            # This file
```

## API

Uses [Open-Meteo](https://open-meteo.com/) - free weather API with no authentication required.

**Endpoint:** `https://api.open-meteo.com/v1/forecast`

Parameters:
- `latitude`: 59.4370
- `longitude`: 24.7536
- `daily`: Weather code, max/min temp, precipitation, wind speed
- `timezone`: Europe/Tallinn
- `forecast_days`: 16 (API limit)

## Build

```bash
npm run build      # Compile TypeScript
npm run dev        # Build and run
npm run test       # Run tests
npm run lint       # Lint code
npm run lint:fix   # Fix linting issues
```

## Weather Conditions

Emojis show current conditions:
- ☀️ Clear
- 🌤️ Mostly Clear
- ⛅ Partly Cloudy
- ☁️ Overcast
- 🌧️ Rain
- ❄️ Snow
- ⛈️ Thunderstorm
- 🌫️ Fog

## Technologies

- **TypeScript** - Type-safe code
- **Axios** - HTTP client
- **Vitest** - Testing framework
- **ESLint** - Code linting

## License

MIT
