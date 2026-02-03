# 🏗️ Baza Troškovnika - Concordia

Centralna baza građevinskih troškovnika s automatskim prepoznavanjem višerednih stavki, masovnim uvozom i cloud dijeljenom bazom.

[![Live Demo](https://img.shields.io/badge/Demo-Live-success)](https://vase-korisnicko-ime.github.io/baza-troskovnika/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 🎯 Značajke

### 💻 Desktop Aplikacija (PRO+)
- ✅ **Masovni uvoz** - Učitajte 20+ Excel troškovnika odjednom
- ✅ **Automatsko prepoznavanje** višerednih stavki i spajanje
- ✅ **Napredna pretraga** - Po opisu, izvoru, jedinici, cijeni, datumu
- ✅ **Pametno pretraživanje** - Prepoznavanje sličnih stavki pri unosu
- ✅ **Izvoz** - Excel, CSV format
- ✅ **Statistika** - Top stavke, usporedbe, prosječne cijene
- ✅ **Praćenje izvora** - Vidi iz kojeg troškovnika dolazi svaka cijena

### 🌐 Web Aplikacija (Shared)
- ✅ **Cloud baza** - Google Sheets kao backend
- ✅ **Dijeljenje s kolegama** - Svi vide istu bazu u realnom vremenu
- ✅ **Samo za pregled** - Kolege mogu pregledavati, ali ne i uređivati
- ✅ **Responzivno** - Radi na desktopu, tabletu, mobitelu
- ✅ **Offline capable** - Desktop verzija radi bez interneta

## 🚀 Brzi Start

### Opcija 1: GitHub Pages (Preporučeno)

**Za kolege - samo pregled:**

1. Posjetite: `https://vase-korisnicko-ime.github.io/baza-troskovnika/`
2. Unesite Sheet ID (dobit ćete ga od admina)
3. Pretražujte bazu!

**Za admina - puno upravljanje:**

1. Preuzmite cijeli repozitorij
2. Otvorite `desktop/Baza_Troskkovnika_PRO_PLUS.html`
3. Uvezite svoje troškovnike
4. Exportajte u Google Sheets za dijeljenje

### Opcija 2: Lokalno Korištenje

1. **Klonirajte repozitorij:**
```bash
git clone https://github.com/vase-korisnicko-ime/baza-troskovnika.git
cd baza-troskovnika
```

2. **Otvorite desktop aplikaciju:**
```bash
# Otvorite u browseru:
desktop/Baza_Troskkovnika_PRO_PLUS.html
```

3. **Ili koristite Python skripte:**
```bash
pip install pandas openpyxl
python scripts/clean_troskovnici.py vase_datoteke.xlsx
python scripts/export_to_google_sheets.py vasa_baza.xlsx
```

## 📁 Struktura Projekta

```
baza-troskovnika/
├── index.html                              # Web app (hosted on GitHub Pages)
├── desktop/
│   ├── Baza_Troskkovnika_PRO_PLUS.html    # Desktop aplikacija
│   └── Troskkovnici_Predlozak_v2.xlsx     # Excel predložak
├── scripts/
│   ├── clean_troskovniki.py               # Čišćenje višerednih stavki
│   └── export_to_google_sheets.py         # Export u Google Sheets
├── docs/
│   ├── UPUTE_Dijeljena_Baza.md            # Detaljne upute
│   └── UPUTE_Python_skripta.md            # Upute za skripte
└── README.md                               # Ova datoteka
```

## 📖 Dokumentacija

### Brzo Postavljanje Google Sheets Backend

1. **Kreirajte Google Sheet:**
   - Idite na [Google Sheets](https://sheets.google.com)
   - Novi blank spreadsheet: "Baza_Troskkovnika_Concordia"
   - Prvi red: `Datum unosa | Izvor | Red. broj | Opis stavke | Jed. mjere | Količina | Jedinična cijena | Ukupna cijena`

2. **Napravite javnim (View-Only):**
   - Share → "Anyone with the link" → "Viewer"
   - Kopirajte Sheet ID iz URL-a

3. **Exportajte podatke:**
   ```bash
   python scripts/export_to_google_sheets.py vasa_baza.xlsx
   # Kopirajte rezultat u Google Sheet
   ```

4. **Konfigurirajte web app:**
   - Otvorite `index.html` (ili hosted verziju)
   - Unesite Sheet ID
   - Gotovo!

Detaljne upute: [UPUTE_Dijeljena_Baza.md](docs/UPUTE_Dijeljena_Baza.md)

## 🎨 Primjeri Korištenja

### Masovni Uvoz Troškovnika

```javascript
// Otvorite desktop/Baza_Troskkovnika_PRO_PLUS.html
// Tab: "Masovni Uvoz"
// Odaberite 20+ Excel datoteka (Ctrl+klik)
// Aplikacija automatski:
// - Prepoznaje višeredne stavke
// - Spaja ih u jednu stavku
// - Dodaje u bazu s izvorom
```

### Pretraživanje i Filtriranje

```javascript
// Pretraga: "beton c25/30"
// Filter: Jedinica = "m3"
// Filter: Cijena = 80-100 EUR
// Rezultat: Sve ponude betona između 80-100€ po m3
```

### Usporedba Cijena

```javascript
// Kolega dobije novi troškovnik
// Traži: "pvc cijev dn110"
// Vidi ponude iz 5 različitih projekata:
//   - Projekt A: 7.80 EUR
//   - Projekt B: 8.50 EUR
//   - Projekt C: 9.20 EUR
// Koristi najjeftiniju za novi projekt!
```

## 🛠️ Tehnologije

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Excel Processing:** SheetJS (xlsx.js)
- **Backend:** Google Sheets API (public read-only)
- **Python Scripts:** pandas, openpyxl
- **Hosting:** GitHub Pages (besplatno)

## 📊 Performanse

- **Lokalna baza:** 10,000+ stavki bez problema
- **Google Sheets:** Do 1,000 stavki (preporučeno za najbolje performanse)
- **Masovni uvoz:** ~30 datoteka u 60 sekundi
- **Pretraga:** Instant filtriranje (client-side)

## 🔒 Sigurnost

- **Desktop aplikacija:** Svi podaci lokalno u browseru (localStorage)
- **Google Sheets:** View-only pristup (kolege ne mogu mijenjati)
- **Privatnost:** Google Sheet može biti javan ili ograničen na određene korisnike

## 🤝 Doprinos

Ovo je interni alat za Concordia. Za sugestije ili bug reports, kontaktirajte IT tim.

## 📝 Licenca

MIT License - slobodno koristite i prilagođavajte za vaše potrebe.

## 📧 Kontakt

**Concordia IT Tim**
- Email: it@concordia.hr
- Web: https://concordia.hr

---

**Verzija:** 2.0  
**Zadnje ažuriranje:** 2025-02-03  
**Održava:** Concordia IT
