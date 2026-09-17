# 💾 LocalStorage String Saver

Egy egyszerű, modern és reszponzív egyoldalas webalkalmazás, amely lehetővé teszi tetszőleges szöveg eltárolását a böngésző helyi tárolójában (`localStorage`). Az elmentett adat az oldal frissítése vagy a böngésző bezárása után is megmarad.

A projekt kifejezetten **GitHub Pages** alatti közvetlen futtatásra lett tervezve, külső építési lépések (build process) vagy backend szerver nélkül.

---

## ✨ Főbb funkciók

- **Helyi adattárolás:** A szöveg a böngésző `localStorage` funkcióját használja, így nem kerül fel semmilyen külső szerverre.
- **Automatikus betöltés:** Az oldal megnyitásakor azonnal megjelenik a legutóbb elmentett érték.
- **Azonnali visszajelzés:** Vizuális állapotjelzés mentéskor és törléskor.
- **Modern UI:** Tailwind CSS segítségével készült, letisztult sötét (Dark mode) felülettel.
- **Mobilbarát:** Reszponzív kialakítás minden képernyőméretre.

---

## 🛠️ Felhasznált technológiák

- **HTML5**
- **JavaScript (ES6+)** – `localStorage` API
- **Tailwind CSS** (CDN-en keresztül)

---

## 🚀 Használat és GitHub Pages beállítás

### 1. Repository előkészítése
1. Hozz létre egy új tárhelyet (Repository-t) a GitHub-on.
2. Töltsd fel az `index.html` és a `README.md` fájlokat a tárhely gyökérmappájába (`root`).

### 2. GitHub Pages bekapcsolása
1. Nyisd meg a tárhelyedet a GitHub-on.
2. Kattints a felső menüsorban a **Settings** (Beállítások) fülre.
3. A bal oldali sávban válaszd a **Pages** menüpontot.
4. A **Build and deployment** résznél:
   - **Source:** Válaszd a `Deploy from a branch` lehetőséget.
   - **Branch:** Válaszd ki a `main` (vagy `master`) ágat és a `/ (root)` mappát.
5. Kattints a **Save** gombra.
6. 1-2 percen belül a GitHub közzéteszi az oldalt a megadott publikus címen (pl.: `https://felhasznalonev.github.io/repo-nev/`).

---

## 💻 Helyi futtatás (Local Development)

Mivel az alkalmazás nem igényel build folyamatot vagy szervert:
1. Töltsd le a projektet.
2. Dupla kattintással nyisd meg az `index.html` fájlt bármelyik böngészőben.

---

## 📄 Licenc

Ez a projekt nyílt forráskódú, és szabadon felhasználható, módosítható a [MIT Licenc](LICENSE) feltételei szerint.
