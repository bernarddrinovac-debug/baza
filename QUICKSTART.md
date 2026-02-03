# ⚡ QUICK START - 5 MINUTA

## Za Admina (Prvi Put)

### 1. Postavite Google Sheet Backend (5 min)

```
1. Idi na: https://sheets.google.com
2. Novi sheet: "Baza_Troskkovnika_Concordia"
3. Prvi red: Datum unosa | Izvor | Red. broj | Opis | Jed | Količina | Cijena | Ukupno
4. Share → Anyone with link → Viewer
5. Copy Sheet ID (iz URL-a između /d/ i /edit)
```

### 2. Upload na GitHub (5 min)

```
1. GitHub → New repository: "baza-troskovnika"
2. Upload sve datoteke iz ovog foldera
3. Settings → Pages → Source: main branch, / (root)
4. Pričekaj 3 minute → Live na: https://tvoj-username.github.io/baza-troskovnika/
```

### 3. Dodaj Sheet ID u kod (2 min - OPCIONALNO)

```
Editiraj index.html, linija ~344:
const savedSheetId = localStorage.getItem('sheetId') || 'TVOJ_SHEET_ID';
```

✅ **Gotovo! Šalji link kolegama.**

---

## Za Kolege (Prvo Korištenje)

### Opcija A: Web verzija (jednostavno)

```
1. Otvori: https://tvoj-username.github.io/baza-troskovnika/
2. Unesi Sheet ID (ako admin nije dodao u kod)
3. Pretražuj!
```

### Opcija B: Desktop verzija (napredne funkcije)

```
1. Preuzmi repozitorij: Download ZIP
2. Otvori: desktop/Baza_Troskkovnika_PRO_PLUS.html
3. Uvezi Excel datoteke (masovni uvoz)
4. Sve radi offline!
```

---

## Svakodnevno Korištenje

### Admin - Ažuriranje baze:

```
1. Otvori desktop/Baza_Troskkovnika_PRO_PLUS.html
2. Uvezi nove troškovnike (Tab: Masovni Uvoz)
3. Exportaj u Excel (Izvezi SVE stavke)
4. Kopiraj nove redove u Google Sheet
✅ Kolege vide update odmah!
```

### Kolege - Pretraživanje:

```
1. Otvori web stranicu
2. Traži: "beton" → Vidi sve beton ponude
3. Filter: Cijena 80-100 EUR
4. Export odabranih u Excel za novi troškovnik
```

---

## 🎯 Primjer Workflow-a

```
UTORAK - 09:00
Admin: Dobio 5 novih troškovnika
  → Uvozi u desktop app (3 min)
  → Copy-paste u Google Sheet (2 min)

UTORAK - 10:00  
Kolega Marko: Treba ispuniti novi troškovnik
  → Otvara web app
  → Traži stavke
  → Koristi najjeftnije cijene
  → Ušteda: 15% na projektu!
```

---

## 📚 Detaljne Upute

- **GitHub deployment:** [docs/GITHUB_DEPLOYMENT.md](docs/GITHUB_DEPLOYMENT.md)
- **Google Sheets setup:** [docs/UPUTE_Dijeljena_Baza.md](docs/UPUTE_Dijeljena_Baza.md)
- **Python skripte:** [docs/UPUTE_Python_skripta.md](docs/UPUTE_Python_skripta.md)

---

## 🆘 Problemi?

**Web app ne učitava podatke:**
- Provjeri Sheet ID
- Provjeri je li Sheet public (View-Only)
- Klikni F12 → Console → Vidi errors

**Desktop app ne importa Excel:**
- Provjeri format Excela (mora biti .xlsx)
- Provjeri ima li header red
- Otvori konzolu (F12) za detalje

**GitHub Pages ne radi:**
- Pričekaj 3-5 minuta nakon uploada
- Settings → Pages → Provjeri je li enabled
- Actions tab → Vidi deploy status

---

**Need help?** Otvori Issue na GitHubu ili kontaktiraj IT tim.

🚀 **Sretno!**
