# 💾 LocalStorage String Manager

## 📋 Projekt áttekintése

Ez a projekt egy pillekönnyű, kliensoldali webes alkalmazás, amely tetszőleges karaktersorozat (string) perzisztens tárolását, megjelenítését és kezelését teszi lehetővé közvetlenül a felhasználó böngészőjében.

A program célja, hogy adatbázis vagy backend szerver jelenléte nélkül, 100%-ban lokális és privát környezetben biztosítson adattárolási funkciót.

---

## ⚙️ Működési elv és Architektúra

Az alkalmazás egyetlen, önálló HTML5 fájlból áll (`index.html`), amely magában foglalja a vizuális elrendezést, a stílusokat és az alkalmazáslogikát.

### 1. Adattárolási logika (`localStorage` API)
- **Kliensoldali perzisztencia:** Az adatokat a böngésző natív `window.localStorage` objektuma tárolja egy meghatározott kulcs (`my_saved_string`) alatt.
- **Élettartam:** Az eltárolt string nem törlődik a böngésző bezárásakor vagy az oldal újratöltésekor. Az adat mindaddig megmarad, amíg a felhasználó manuál দিগan nem törli azt az alkalmazáson keresztül, vagy nem üríti a böngészője gyorsítótárát.
- **Adatvédelem és Biztonság:** Az adatok kizárólag a felhasználó saját eszközén tárolódnak, semmilyen hálózati kérés (HTTP request) vagy külső API felé nem továbbítódnak.

### 2. Felhasználói felület és Állapotkezelés
- **Automatikus inicializálás:** Az oldal betöltésekor a rendszer kiolvassa a tárolt értéket, és azonnal szinkronizálja a beviteli mezőt, valamint az előnézeti panelt.
- **Dinamikus visszajelzések:**
  - **Üres állapot:** Ha nincs tárolt adat, az előnézeti panel egy dőlt betűs, halvány jelzést jelenít meg.
  - **Mentési állapot:** Mentéskor az előnézet frissül, és a felületen megjelenik egy animált, zöld színű sikeres mentés jelzés.
  - **Törlési állapot:** A törlés gomb megnyomásakor a kulcs törlődik a tárolóból, a felület pedig visszaáll az alapértelmezett üres állapotra.

---

## 🎨 Vizuális kialakítás

- **Keretrendszer:** Tailwind CSS (CDN alapon), amely utility-first osztályokkal építi fel a felületet.
- **Téma:** Sötét mód (Dark mode) kontrasztos, mélykék és szürke színárnyalatokkal (`slate-900`, `slate-800`), amely csökkenti a szem terhelését.
- **Elrendezés:** Flexbox alapú, kártya jellegű központi elrendezés, amely mobilon és asztali kijelzőkön is reszponzív.

---

## 🛠️ Technológiai struktúra

| Komponens | Használt technológia | Szerep a programban |
| :--- | :--- | :--- |
| **Szerkezet (Markup)** | HTML5 | A beviteli mező (`<textarea>`), az akciógombok és az előnézeti panelek struktúrája. |
| **Stílus (Styling)** | Tailwind CSS | A reszponzív elrendezés, sötét téma, tipográfia és gomb-interakciók stílusa. |
| **Logika (Script)** | Vanilla JavaScript (ES6+) | Eseménykezelés (Event Listeners), DOM-manipuláció és a `localStorage` kezelése. |
| **Adatréteg (Storage)** | Web Storage API | Kliensoldali kulcs-érték (key-value) pár alapú adattárolás. |
