# [fit] A Weather Station,
# [fit] Plant Monitors,
# [fit] Buttons,
# [fit] and Other Smart Home Fun

---

# Amateur
## Former Full Time Software Engineer

- A long time ago I was a full stack web developer
- Long and slow migration to web frontend
- Long and slow migration to functional programming and strongly typed languages
- Mostly a stay-at-home Dad now
- Less time in front of my computer
- More variety of technology projects

---

# [fit] A Little bit about "self hosting" and "local first"

- "local first" means "it still works with no Internet"
- "self hosting" means "it is in my house"
- Running locally is a priority for me
- You need to run some infrastructure in your home
- Self hosting is fun
- I lean heavily on TrueNAS Scale
- Talk more later

---

# [fit] Weather Station

---

> Why would I want my own weather station?
-- Just about everyone with a smart phone

---

## The actual weather

 - Sometimes the weather at your house is different than the weather at the closest weather station
 - Growing Degree Days

## Contributing to weather data

## Fun

---

# [fit] Ambient Weather WS-2902D Web G

![inline](/Users/jachin/Documents/speaking/minnebar 2026/aw-ws-2902.jpg.webp)

---

# How it works

Weather station communicates of a special wireless link the base station.

The base station tries to send your weather data to the cloud (where you can use their app)

But you're not exactly locked in. You can point the base station at any URL, but it has to mimic the API of either AmbientWeather or Wunderground. Which, as these things go, is fine, just _fine_.

---

# Self Hosting the Weather Data

# Weather Station Data Collector

And then, the world!

---

# Weather Station Data Collector

## Easy to build

 - Behold the power of LLMs
 - Re implement an existing API (no problem)

## Extra polish

 - Wrap it all up in a Docker image
 - APIs for getting the weather data out

---

# To my TRMNL

I talked last year about TRMNL

Built a plugin

---

# Windmill

![inline](/Users/jachin/Documents/speaking/minnebar 2026/windmill_icon.svg)

> Code-first orchestration platform for internal software

---

# Windmill

- Fancy Cron
- "Update my TRMNL plugin with the latest weather from my weather station every 15 minutes"
- Easy to install (and update) on TrueNAS
- Way more than I need (but thoughtfully designed so it's not hard to use)
- Lots of other things out there to do this

---

# The Whole Solution

```pikchr
WS: box rad 10px "🌦️ Weather Station" fit
arrow right 200% "AmbientWeather HTTP API" above
DC: box rad 10px "📡 Weather Station" "Data Collector" fit
arrow down 200% "HTTP API" aligned above
WM: box rad 10px "🔄 Windmill" fit
arrow left 500% "Web Hooks with JSON Payloads" above
TP: box rad 10px "🖥️ TRMNL Plugin" fit
```

---

# Weather Station TODOs

- Weather Station data collector
  - Not quite reliable enough
  - Better APIs
  - Data Roll up
- TRMNL
  - Self Host TRMNL Software
  - Better looking plugin

---

# [fit] Plant Monitors
# [fit] 🌱👀

---

I intend to make my own, someday

(Maybe a picture of parts)

---

# Apollo Automation

Function, 3D printed stuff


---

# PLT-1

A plant monitor you don't have to build your self

ESPHome

Super easy to setup

I like the power options (rechargeable battery or plugin)

The hard part is figuring out how make the data useful

Knowing what the soil moisture is ≠ knowing when to water your plants

---

Data vs Solutions

---

# BTN-1

## Apollo Automation

4 Buttons plus lights

---

# Maybe over did it on the buttons

Once you start thinking in terms of "scenes" and not turning this or that thing on, maybe you don't need button.

---

# Bed Time

## 1 Button cycles through 4 scenes

### Getting ready for bed

### Winding Down

### Sleeping

 - White noise machine (off)
 - Book shelf LED strip (very dim)
 - Book lamp (off)

### Wake up (Everything off

 - White noise machine (off)
 - Book shelf LED strip (off)
 - Book lamp (off)