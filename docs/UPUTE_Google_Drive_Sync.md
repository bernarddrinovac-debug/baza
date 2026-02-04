# 📂 GOOGLE DRIVE SYNC - UPUTE

## 🎯 Što ova skripta radi?

1. **Čita SVE Excel datoteke** iz vašeg Google Drive foldera
2. **Automatski prepoznaje i spaja** višeredne stavke
3. **Generira konsolidiranu bazu** u jedan Excel
4. **Vi samo copy-paste** u Google Sheet

---

## 🚀 SETUP (PRVI PUT) - 5 minuta

### Korak 1: Instalirajte Python (ako nemate)

**Windows:**
1. Download: https://www.python.org/downloads/
2. Install → ✅ Označite "Add Python to PATH"
3. Restart računala

**Mac/Linux:**
Python je već instaliran!

### Korak 2: Instalirajte potrebne biblioteke

Otvorite **Command Prompt** (Windows) ili **Terminal** (Mac/Linux):

```bash
pip install gdown pandas openpyxl --break-system-packages
```

Ako ne radi, pokušajte:
```bash
python -m pip install gdown pandas openpyxl
```

### Korak 3: Preuzmite skriptu

Preuzmite `google_drive_sync.py` iz chata i stavite ga bilo gdje na računalu (npr. Desktop).

---

## 📋 SVAKODNEVNA UPORABA

### Workflow:

```
1. Dobijete novi troškovnik (Excel)
   ↓
2. Upload u Google Drive folder: Troskovnici_Import
   ↓
3. Pokrenite skriptu (dvostruki klik ili iz Command Prompt)
   ↓
4. Skripta downloadа SVE Excele iz foldera
   ↓
5. Procesira ih (spaja višeredne stavke)
   ↓
6. Generira: Konsolidirana_Baza.xlsx
   ↓
7. Vi otvorite taj Excel
   ↓
8. Ctrl+A → Ctrl+C (kopirajte sve)
   ↓
9. Zalijepite u Google Sheet (od A2)
   ↓
10. Osvježite web app → Kolege vide nove podatke!
```

---

## 🖱️ Pokretanje skripte

### Opcija A: Dvostruki klik (Windows)

1. Desni klik na `google_drive_sync.py`
2. "Open with" → "Python"
3. Skripta se pokrene automatski

### Opcija B: Command Prompt / Terminal

```bash
cd C:\put\do\skripte
python google_drive_sync.py
```

---

## 📊 Što skripta radi?

```
╔══════════════════════════════════════════════════════════════╗
║     GOOGLE DRIVE SYNC - BAZA TROŠKOVNIKA                    ║
╚══════════════════════════════════════════════════════════════╝

📥 Downloadam datoteke iz Google Drive foldera...
   Folder ID: 1b15lwmzDNYWNf8Zj20jdMRdmgTW8gO7j
✅ Download završen!

══════════════════════════════════════════════════════════════
📊 PROCESIRANJE 15 EXCEL DATOTEKA
══════════════════════════════════════════════════════════════

📄 Troskovnik_Skola_ABC...
   ✅ 25 stavki (3 spojeno)
📄 Troskovnik_Vrtic_XYZ...
   ✅ 18 stavki (1 spojeno)
📄 Troskovnik_Most_123...
   ✅ 42 stavki (5 spojeno)
...

══════════════════════════════════════════════════════════════
✅ USPJEŠNO!
══════════════════════════════════════════════════════════════
📊 Ukupno stavki: 347
🔗 Spojenih višerednih stavki: 43
📁 Procesiranih datoteka: 15
💾 Spremljeno u: Konsolidirana_Baza.xlsx

══════════════════════════════════════════════════════════════
📋 SLJEDEĆI KORACI:
══════════════════════════════════════════════════════════════
1. Otvorite: Konsolidirana_Baza.xlsx
2. Selektirajte SVE (Ctrl+A)
3. Kopirajte (Ctrl+C)
4. Otvorite Google Sheet
5. Zalijepite (Ctrl+V)
6. Osvježite web app

⏎ Pritisnite Enter za zatvaranje...
```

---

## 🔄 Kada pokrenuti skriptu?

### Prvi put:
- Uploadajte 10-20 postojećih troškovnika u Google Drive
- Pokrenite skriptu
- Copy-paste u Google Sheet
- ✅ Baza puna!

### Svaki dan/tjedan:
- Dobijete 2-3 nova troškovnika
- Upload u Google Drive
- Pokrenite skriptu
- Copy-paste **SAMO NOVE REDOVE** u Google Sheet (dodajte na kraj)

### Ili resetirajte cijelu bazu:
- Pokrenite skriptu
- Zalijepite preko starih podataka (zamijeni cijelu bazu)

---

## ⚙️ Konfiguracija

Ako trebate promijeniti Google Drive folder, otvorite `google_drive_sync.py` u Notepad i promijenite liniju:

```python
GOOGLE_DRIVE_FOLDER_ID = "1b15lwmzDNYWNf8Zj20jdMRdmgTW8gO7j"
```

---

## 🐛 Troubleshooting

### Problem: "gdown not installed"
```bash
pip install gdown --break-system-packages
```

### Problem: "Cannot download from Google Drive"
- Provjerite je li folder javan (Anyone with link → Viewer)
- Pokušajte otvoriti folder u browseru
- Provjerite Folder ID

### Problem: "No Excel files found"
- Provjerite imate li .xlsx datoteke u folderu
- Provjerite nisu li datoteke u sub-folderima (skripta čita rekurzivno)

### Problem: "Permission denied"
- Pokrenite Command Prompt kao Administrator

---

## 🎯 Prednosti ovog pristupa

✅ **Jednostavno:** 1 klik za ažuriranje  
✅ **Brzo:** 20 Excela procesira za 30 sekundi  
✅ **Sigurno:** Svi Exceli ostaju u Google Drive (backup)  
✅ **Fleksibilno:** Dodajte/uklonite Excele kad god želite  
✅ **Automatsko čišćenje:** Višeredne stavke se spajaju automatski  

---

## 📧 Podrška

Za probleme, kontaktirajte IT tim ili otvorite Issue na GitHubu.

---

**Verzija:** 1.0  
**Zadnje ažuriranje:** 2025-02-03
