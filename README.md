# 💩 KakAttack - Tisselt 2830

Een ludieke location-based webapp om hondendrollen te rapporteren in Tisselt, België.

![KakAttack Screenshot](https://via.placeholder.com/600x300/FFD93D/4A2C0A?text=💩+KakAttack)

## 🎮 Features

- **📍 GPS Tracking** - Meld drollen op je exacte locatie
- **🔥 Heatmap** - Bekijk waar de meeste drollen liggen  
- **🧭 Navigator** - Vind de meest verse drol in de buurt
- **🏆 Live Leaderboard** - Compete met andere Drollenjagers (Firebase)
- **🦁 Drollensafari** - Premium feature met Professor Poep

## 🚀 Quick Start

### 1. Fork deze repository

Klik op de **Fork** knop rechtsboven.

### 2. Firebase instellen (optioneel maar aanbevolen)

Volg de instructies in **[FIREBASE_SETUP.md](FIREBASE_SETUP.md)** voor een gedeeld leaderboard.

> Zonder Firebase werkt de app lokaal - je ziet alleen je eigen scores.

### 3. GitHub Pages activeren

1. Ga naar je fork's **Settings**
2. Scroll naar **Pages** in het linkermenu
3. Source: **Deploy from a branch**
4. Branch: `main` / `/ (root)`
5. Klik **Save**

### 4. Spelen! 🎉

Na ~2 minuten is je site live op:
```
https://JOUW-USERNAME.github.io/kakattack/
```

## 📱 Installeren als App

KakAttack werkt als Progressive Web App:

1. Open de site op je telefoon
2. **iOS**: Tik op Share → "Zet op beginscherm"
3. **Android**: Tik op menu → "Installeren" of "Toevoegen aan startscherm"

## 🔧 Lokaal Testen

```bash
# Clone je fork
git clone https://github.com/JOUW-USERNAME/kakattack.git
cd kakattack

# Start een lokale server (kies een optie)
python -m http.server 8000
# OF
npx serve
# OF
php -S localhost:8000

# Open http://localhost:8000
```

> ⚠️ Geolocation werkt alleen op `localhost` of `https://`

## 📁 Bestandsstructuur

```
kakattack/
├── index.html          # De volledige app (HTML + CSS + JS)
├── FIREBASE_SETUP.md   # Firebase configuratie handleiding
├── README.md           # Dit bestand
└── .gitignore          # Git ignore regels
```

## 🎯 Hoe het werkt

1. **Start** - Voer je naam in en start de jacht
2. **Zoek** - Loop door Tisselt en zoek naar hondendrollen
3. **Meld** - Druk op de grote 💩 knop om te rapporteren
4. **Kies** - Selecteer grootte en versheid
5. **Scoor** - Verdien punten en klim in de ranks!

### Punten Systeem

| Actie | Punten |
|-------|--------|
| Drol melden | 10 pts |
| Combo x2 | +5 bonus |
| Combo x3 | +10 bonus |
| Combo x4+ | +15+ bonus |

### Ranks

| Meldingen | Rank |
|-----------|------|
| 0+ | Beginnende Speurder |
| 5+ | Drol Detective |
| 15+ | Kak Kapitein |
| 30+ | Poop Patrouilleur |
| 50+ | Stront Specialist |
| 100+ | Meester Drollenjager |
| 200+ | Legende van Tisselt |

## 🛠️ Technologie

- **HTML5** - Single-file webapp
- **CSS3** - Responsive design, animaties
- **JavaScript** - Vanilla JS, geen frameworks
- **Leaflet.js** - OpenStreetMap kaart
- **Firebase** - Realtime Database (optioneel)
- **Geolocation API** - GPS tracking

## 📍 Locatie

**Tisselt**, Postcode 2830, België
- Coördinaten: 51.0547, 4.3833
- Gemeente: Willebroek

## ⚠️ Vereisten

- **HTTPS** - Verplicht voor GPS (GitHub Pages doet dit automatisch)
- **Moderne browser** - Chrome, Firefox, Safari, Edge
- **Locatie toegang** - Moet toegestaan worden in de browser

## 🤝 Bijdragen

Pull requests zijn welkom! Voor grote wijzigingen, open eerst een issue.

## 📄 Licentie

MIT License - Vrij te gebruiken en aan te passen.

## 🙏 Credits

- Kaart data: [OpenStreetMap](https://www.openstreetmap.org/)
- Icons: Emoji's
- Fonts: [Google Fonts](https://fonts.google.com/) (Bangers, Nunito)
- Database: [Firebase](https://firebase.google.com/)

---

**Made with 💩 in Tisselt**

*Disclaimer: Dit is een satirisch project om een lokaal probleem onder de aandacht te brengen. Ruim altijd de drollen van je hond op!*
