# Quick Weather ⚡️☁️

A simple weather app built with HTML & CSS. It fetches current weather data from the OpenWeather API and displays temperature, humidity, wind speed and an icon that reflects weather condition.

## Features
- City search with button click
- Enter-key search and debouncing feature
- Shows temperature (°C), humidity (%), and wind speed
- Weather icons for Clouds, Clear, Rain, Drizzle, Mist & Snow
- Basic error state for invalid city names

## Project Structure
- [index.html](index.html): Markup and app script
- [style.css](style.css): Styles
- [images/](images): Icons 

## Prerequisites
- An OpenWeather API key: https://openweathermap.org/api
- Internet connection

## Setup
1. Open [index.html](index.html) and replace the placeholder API key:
	```js
	const apiKey = "YOUR_API_KEY_HERE";
	```
2. Ensure the icons listed above exist under [images/](images).

## Run Locally (macOS)
You can open the app directly or run a tiny local server.

Option A — Open file directly:
```bash
open index.html
```

Option B — VS Code Live Server:
- Install the “Live Server” extension in VS Code
- Open this folder and click “Go Live”

Option C — Python HTTP server:
```bash
cd /Users/nadildulran/MyWork/WeatherAPP/quickweather
python3 -m http.server 5500
# Then open http://localhost:5500
```

## Usage
1. Enter a city name in the input.
2. Click the search button.
3. The card updates with the city, temperature, humidity, wind speed and the appropriate weather icon. Invalid cities show an error message.

## Notes & Troubleshooting
- Units: The app requests metric units. OpenWeather returns wind speed in m/s for metric. If you want km/h, multiply by 3.6 before displaying.
- Invalid city: Shows the error section and hides the weather card.
- API rate limits: If requests stop working temporarily, you may have hit free-tier limits.
- Mixed content: Requests use HTTPS, so it should work fine when served locally or from file.
