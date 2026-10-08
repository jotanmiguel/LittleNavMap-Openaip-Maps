# OpenAIP VFR Map Theme (v1.2 - Beta)

A custom **DGML map theme for Little Navmap** that combines a **OpenStreetMap / OpenTopoMap** basemap with the **OpenAIP aeronautical data overlay** (airspaces, aerodromes, navaids, obstacles), inspired by the clean visual style used on the official OpenAIP platform.

---

## ⚠️ Status: v1.2 — Beta

This is a functional initial release, currently undergoing testing and refinement. 

* A fully custom basemap is planned for a future release to closely replicate the native OpenAIP visual identity.
* **Feedback and bug reports are welcome!**
* Working on a way to dismiss the need to create an openaip account for every user. 

---

## 🗺️ Features

* **High-Detail Different Basemaps:** Topographic / Mapbox background with clear terrain features and geographic reference points, with more being added in the future upon request.
* **OpenAIP Aeronautical Overlay:** Live VFR airspaces, airports, airfields, radio navaids, and reporting points via the official OpenAIP API.
* **Obstacles & Hotspots Layer:** Vertical obstructions, wind turbines, communication towers, masts, chimneys, and lighthouses rendered with transparent overlay blending (`OverpaintBlending`).

---

## 🔑 Prerequisites & API Keys

This theme requires your own API keys to function properly:
1. **OpenAIP API Key** *(Free)* — Required for aeronautical overlays.

> **Note:** This project is an independent community add-on and is **not affiliated with, endorsed by, or connected to** OpenStreetMap, OpenTopoMap or OpenAIP.

---

## 📥 Installation Guide

1. **Get an OpenAIP API Key:**
   * Create a free account at [OpenAIP.net](https://www.openaip.net/).
   * Navigate to **Profile → API Clients** and create a new API Client.
   * Copy your generated **API Key**.

2. **Configure the DGML File:**
   * Open the `openaip-map.dgml` from the theme you want to use (`openaip-map.dgml`, `openaip-map-topo.dgml`, etc) in any text editor.
   * Find the placeholder `YOUR_OPENAIP_API_KEY` inside the `<downloadUrl>` tag. 
        > Tip: Use the find function (Ctrl + F) to find the placeholder.
   * Replace `YOUR_OPENAIP_API_KEY` with your actual OpenAIP key:
     ```xml
     path="/api/data/openaip/{zoomLevel}/{x}/{y}.png?apiKey=YOUR_ACTUAL_KEY_HERE"
     ```
     > Tip: Using the find function (Ctrl + F), you could also replace every occurrence of `YOUR_ACTUAL_KEY_HERE` with your key.

1. **Install into Little Navmap:**
   * Extract the map theme folder.
   * Copy the theme folder to your Little Navmap themes directory:
     * **Windows:** `Documents\Little Navmap Files\Map Themes\`
     * **macOS:** `~/Documents/Little Navmap Files/Map Themes/`
     * **Linux:** `~/.local/share/Little Navmap/Map Themes/` or `~/Documents/Little Navmap Files/Map Themes/`
   * Restart **Little Navmap**.
   * Select the **OpenAIP Map** you installed from the map theme dropdown menu.

---

## 📜 Attributions & Data Sources

This add-on utilizes third-party maps and data services:

* **Aeronautical Data (TMS/MVT):** © [OpenAIP](https://www.openaip.net)
* **Basemap Data:** © [OpenTopoMap](https://opentopomap.org) (CC-BY-SA) · © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright)

---

## 📝 Changelog

* **v1.2** - New map theme added:
  * OpenTopoMap added as requested by a user.
  * Updated so it´s now a package of themes (currently with two - OpenStreetMap and OpenTopoMap).
* **v1.1** — Description & Documentation update:
  * Clarified step-by-step installation instructions.
  * Updated API key configuration guidelines.
* **v1.0** — Initial Beta Release:
  * First functional release featuring OpenAIP overlay integration.