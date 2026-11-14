---
name: weather-brief
description: Short weather brief for a city (today, tonight, tomorrow) with what it means for the day's plans. Uses the weather_forecast tool, or web search when that tool is missing.
version: 0.1.0
author: CSCI 599 HW3
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Weather, Briefing, Open-Meteo]
    homepage: https://open-meteo.com/en/docs
---

# Weather brief

Produce at most three bullet points about the weather for one city (default: the user's city
from their profile; Los Angeles if unknown).

## Get the data
1. If a `weather_forecast` tool is available, call `weather_forecast(city, days=2)`.
   It returns current conditions plus daily high, low and chance of rain from Open-Meteo.
2. If there is no such tool, or it returns an error (Open-Meteo can time out), call `web_search`
   with `"<city> weather forecast today"` and read the high, low and chance of rain from the
   results. Say that the numbers came from a web search.

## Write the brief
- Bullet 1: now — temperature and conditions.
- Bullet 2: today — high / low and chance of rain.
- Bullet 3 (only if useful): what to plan for, e.g. "rain after 3 pm: bring an umbrella to the
  interview", or tomorrow's change if it is large (more than about 10 °F or rain starting).
- Use the units the tool returns. Do not invent numbers; if no data came back, say so in one line.
