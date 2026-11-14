# hermes-weather-brief

A [Hermes Agent](https://github.com/NousResearch/hermes-agent) skill tap with one skill,
**weather-brief**: a short weather brief for a city (now, today, tomorrow) and what it means for
the day's plans.

The skill uses a `weather_forecast` tool when the agent has one (for example a plugin that calls
Open-Meteo). Without that tool it uses Hermes' `web_search` and says that the numbers came from a
web search. It needs no API key of its own and stores nothing.

Written for a course assignment (CSCI 599, Assignment 3). No personal data, credentials or
machine-specific paths.

## Install

```sh
hermes skills tap add PanLu09/hermes-weather-brief
hermes skills install PanLu09/hermes-weather-brief/skills/weather-brief
```

Then ask the agent, for example: `Give me a weather brief for Los Angeles.`

Tested with Hermes v0.21.5 (tag `v2026.9.24`).

## Layout

```
skills/
  weather-brief/
    SKILL.md
```

## License

MIT, see [LICENSE](LICENSE).
