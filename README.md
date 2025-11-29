# 💩 KakAttack - Tisselt 2830

Een ludieke location-based webapp om hondendrollen te rapporteren in Tisselt, België.

## 🎮 Features

- **📍 GPS Tracking** - Meld drollen op je exacte locatie
- **🔥 Heatmap** - Bekijk waar de meeste drollen liggen
- **🧭 Navigator** - Vind de meest verse drol in de buurt
- **🏆 Leaderboard** - Compete met andere Drollenjagers
- **🦁 Drollensafari** - Premium feature met Professor Poep

## 🚀 Live Demo

👉 **[https://JOUW-USERNAME.github.io/kakattack/](https://JOUW-USERNAME.github.io/kakattack/)**

## 📦 Installatie

### Optie 1: Fork & Deploy

1. Fork deze repository
2. Ga naar **Settings → Pages**
3. Onder "Source" kies **Deploy from a branch**
4. Selecteer `main` branch en `/ (root)`
5. Klik **Save**
6. Wacht ~2 minuten, je site is live!

### Optie 2: Lokaal testen

```bash
git clone https://github.com/JOUW-USERNAME/kakattack.git
cd kakattack
# Open index.html in je browser
# OF gebruik een lokale server:
python -m http.server 8000
# Open http://localhost:8000
```

## 🔥 Firebase Setup (Optioneel)

Voor een gedeeld leaderboard:

1. Ga naar [console.firebase.google.com](https://console.firebase.google.com)
2. Maak een nieuw project
3. Activeer **Realtime Database** (Europe)
4. Kopieer je config naar `index.html`
5. Zet deze database rules:

```json
{
  "rules": {
    "leaderboard": {
      ".read": true,
      ".write": true,
      ".indexOn": ["score"]
    }
  }
}
```

## 📱 PWA Support

De app werkt als Progressive Web App:
- Installeerbaar op mobiel
- Werkt offline (basis functionaliteit)
- GPS tracking voor real-time locatie

## 🛠️ Technologie

- **HTML5** - Single-file webapp
- **Leaflet.js** - OpenStreetMap integratie
- **Firebase** - Realtime Database (optioneel)
- **Geolocation API** - GPS tracking

## 📍 Locatie

Tisselt, Postcode 2830, België
- Coördinaten: 51.0547, 4.3833

## ⚠️ Vereisten

- **HTTPS** - Geolocation werkt alleen via HTTPS (GitHub Pages doet dit automatisch)
- **Moderne browser** - Chrome, Firefox, Safari, Edge

## 📄 Licentie

MIT License - Vrij te gebruiken en aan te passen!

---

Made with 💩 in Tisselt
