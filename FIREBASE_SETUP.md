# 🔥 Firebase Setup Handleiding

Volg deze stappen om je eigen Firebase database te koppelen aan KakAttack.

## Stap 1: Firebase Account

1. Ga naar [console.firebase.google.com](https://console.firebase.google.com/)
2. Log in met je Google account (maak er een aan als je er geen hebt)

## Stap 2: Nieuw Project Aanmaken

1. Klik op **"Create a project"** of **"Add project"**
2. Geef je project een naam: `kakattack` (of iets anders)
3. Google Analytics mag je **uitschakelen** (niet nodig)
4. Klik **"Create project"**
5. Wacht tot het klaar is en klik **"Continue"**

## Stap 3: Realtime Database Aanmaken

1. In het linkermenu, klik op **"Build"** → **"Realtime Database"**
2. Klik **"Create Database"**
3. Kies locatie: **Belgium (europe-west1)** ⚠️ BELANGRIJK!
4. Start in **"test mode"** (we passen rules later aan)
5. Klik **"Enable"**

## Stap 4: Database Rules Instellen

1. Ga naar het **"Rules"** tabblad in je Realtime Database
2. Vervang de regels met:

```json
{
  "rules": {
    "leaderboard": {
      ".read": true,
      ".write": true,
      ".indexOn": ["score", "lastActive"]
    },
    "reports": {
      ".read": true,
      ".write": true,
      ".indexOn": ["timestamp"]
    }
  }
}
```

3. Klik **"Publish"**

> ⚠️ Deze rules zijn open voor development. Voor productie wil je authenticatie toevoegen!

## Stap 5: Web App Toevoegen

1. Ga naar **Project Overview** (klik op het huisje linksboven)
2. Klik op het **web icoon** (`</>`) om een web app toe te voegen
3. Geef de app een naam: `KakAttack Web`
4. **Firebase Hosting** hoeft NIET aangevinkt (we gebruiken GitHub Pages)
5. Klik **"Register app"**

## Stap 6: Config Kopiëren

Nu zie je je Firebase configuratie. Het ziet er zo uit:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyB1234567890abcdefg",
  authDomain: "kakattack-12345.firebaseapp.com",
  databaseURL: "https://kakattack-12345-default-rtdb.europe-west1.firebasedatabase.app",
  projectId: "kakattack-12345",
  storageBucket: "kakattack-12345.appspot.com",
  messagingSenderId: "123456789012",
  appId: "1:123456789012:web:abcdef123456"
};
```

## Stap 7: Config Invullen in index.html

1. Open `index.html` in een teksteditor
2. Zoek naar dit blok (rond regel 350):

```javascript
const FIREBASE_CONFIG = {
    apiKey: "JOUW_API_KEY_HIER",
    authDomain: "JOUW_PROJECT_ID.firebaseapp.com",
    ...
};
```

3. Vervang de placeholder waarden met jouw echte waarden uit stap 6
4. Sla het bestand op

## Stap 8: Testen

1. Upload naar GitHub (zie README.md)
2. Open je site via GitHub Pages
3. Rechtsonder zie je de status:
   - **"Online"** (groen) = Firebase werkt! 🎉
   - **"Offline"** (oranje) = Check je config
   - **"Lokaal"** (oranje) = Config niet ingevuld

## Troubleshooting

### "Permission denied" error
- Check je Database Rules (stap 4)
- Zorg dat je in "test mode" zit

### Database URL error
- Controleer of je **europe-west1** hebt gekozen
- De URL moet eindigen op `.europe-west1.firebasedatabase.app`

### Leaderboard laadt niet
- Open browser console (F12) voor errors
- Check of alle config waarden correct zijn gekopieerd

## Gratis Limieten

Firebase Spark plan (gratis) geeft je:
- **1 GB** database opslag
- **10 GB/maand** data transfer
- **100 simultane connecties**

Meer dan genoeg voor KakAttack! 💩

---

## Hulp nodig?

- [Firebase Docs](https://firebase.google.com/docs/database)
- [Firebase Console](https://console.firebase.google.com/)
