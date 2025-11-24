# Weather Intelligence - Immersive Forecast

## Purpose
Generates a vivid, time-aware weather forecast with explicit timezone handling and practical impact guidance. Designed to feel like a professional broadcast meteorologist briefing, not a data dump.

## Use Cases
- Daily weather planning for location-specific activities
- Travel preparation and logistics
- Outdoor event planning
- Time-zone aware weather updates (especially for remote teams)

## Instructions
1. Paste this prompt to get today's weather forecast
2. Modify the location (default: Denver, Colorado) and timezone (default: America/Denver)
3. AI will first establish current local time, then provide immersive forecast
4. Includes practical impacts for daily activities (driving, outdoor plans, etc.)

---

## The Prompt

```text
Act as a seasoned broadcast meteorologist.

Task:
Generate an **immersive, vivid weather update** for **Denver, Colorado** for today.

Requirements:
- First, determine the **current UTC time** and convert it to **America/Denver**.
- At the very top, state:
  "Report generated at: [LOCAL 24h time] on [LOCAL date] (Mountain Time)."

Content:
1. **Headline Overview (2–3 sentences)**
   - The main story (e.g., storm system, cold front, heat dome).

2. **Morning / Afternoon / Evening / Overnight**
   - Short paragraph each: temperature ranges, wind, precipitation, and cloud cover.

3. **Impacts & Advice**
   - 3–5 bullets for a normal working day: driving, outdoor plans, kids, pets, etc.

Style:
- Vivid but clear; no fear-mongering.
- No Celsius conversions.
- Remember: I'm in Mountain Time; don't describe it as "night" for me if it's only night in UTC.
```

---

## Customization Notes

**Location Options** (replace Denver, Colorado with):
- Any US city: "Seattle, Washington", "Austin, Texas", "Miami, Florida"
- International cities: "London, UK", "Tokyo, Japan", "Sydney, Australia"
- Specific neighborhoods: "Brooklyn, New York", "Mission District, San Francisco"

**Timezone Handling**:
- Default: America/Denver (Mountain Time)
- Common alternatives: America/New_York, America/Los_Angeles, America/Chicago
- International: Europe/London, Asia/Tokyo, Australia/Sydney

**Forecast Detail Levels**:
- Standard: Morning/Afternoon/Evening/Overnight
- Detailed: Add "Late Night" and specific hour-by-hour for critical periods
- Minimal: Just "Today" and "Tonight" with highlights

---

## Recommended Improvements

### Potential Enhancements
1. **Multi-Day Lookahead**: Add 3-day or 7-day extended forecast option
2. **Activity-Specific**: Custom impact sections (cycling, hiking, photography, sports)
3. **Severe Weather Alerts**: Prominent callout for watches/warnings with timing
4. **Historical Context**: Compare to typical conditions or notable past events
5. **Pollen/Air Quality**: Add allergen and AQI information for health planning
6. **Hyperlocal**: Support multiple microclimates in metro areas (mountains vs city)

### Questions for Discussion
- Should this pull real-time weather data or rely on AI's training knowledge?
- Add sunrise/sunset times and moon phase for outdoor planning?
- Include "what to wear" guidance based on temperature and activity?
- Support "travel mode" with multi-city forecasts for trips?
- Add weather personality modes (technical, poetic, minimalist)?
- Include "weather decision framework" for go/no-go on outdoor activities?
