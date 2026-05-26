# Garderobe Stundenzettel PWA

Eine Progressive Web App zur Zeiterfassung für Garderobiere. 

## Features

- ⏱️ **Timer-Modus**: Live-Zeitmessung mit Start/Stop
- ✎ **Manueller Eintrag**: Freie Eingabe von Datum, Zeit und Pause
- 📊 **Übersichten**: Tages-, Wochen- und Monatsansichten
- 💾 **Persistenz**: Alle Daten werden lokal gespeichert
- 📥 **CSV-Export**: Download aller Einträge als CSV-Datei
- 📱 **Offline-fähig**: Funktioniert auch ohne Internetverbindung
- 🏠 **Installierbar**: Kann als App auf dem Homescreen installiert werden

## Deployment auf GitHub Pages

### 1. GitHub Repository erstellen

1. Gehe zu [github.com](https://github.com) und logge dich ein
2. Klicke auf das **+** oben rechts und wähle **New repository**
3. Repository-Name: z.B. `stundenzettel` (wird Teil der URL)
4. Setze auf **Public**
5. **NICHT** "Initialize with README" anklicken
6. Klicke auf **Create repository**

### 2. Dateien hochladen

**Variante A: Über die Web-Oberfläche (einfach)**

1. Im neuen Repository auf **uploading an existing file** klicken
2. Alle Dateien aus diesem Ordner hineinziehen:
   - `index.html`
   - `stundenzettel.jsx`
   - `manifest.json`
   - `sw.js`
   - `icon.png`
   - `icon-192.png`
   - `icon-512.png`
3. Commit message eingeben (z.B. "Initial commit")
4. Auf **Commit changes** klicken

**Variante B: Via Git (fortgeschritten)**

```bash
# Im Ordner mit den Dateien
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/DEIN-USERNAME/stundenzettel.git
git push -u origin main
```

### 3. GitHub Pages aktivieren

1. Gehe in deinem Repository auf **Settings**
2. Klicke links auf **Pages**
3. Unter **Source** wähle **Deploy from a branch**
4. Unter **Branch** wähle `main` und `/root`
5. Klicke auf **Save**

### 4. Warten & Aufrufen

- Nach 1-2 Minuten ist die App unter dieser URL erreichbar:
  ```
  https://DEIN-USERNAME.github.io/stundenzettel/
  ```
- Ersetze `DEIN-USERNAME` mit deinem GitHub-Benutzernamen
- Ersetze `stundenzettel` mit deinem Repository-Namen

### 5. Als App installieren

**Auf dem Smartphone:**
- **iOS**: Safari → Teilen-Button → "Zum Home-Bildschirm"
- **Android**: Chrome → Menü (⋮) → "Zum Startbildschirm hinzufügen"

**Desktop:**
- **Chrome/Edge**: Adressleiste → Install-Icon (⊕) rechts neben dem Stern

## Aktualisierungen

Wenn du die App später ändern möchtest:

1. Bearbeite die Dateien im Repository (über Web-Interface oder Git)
2. Commit & Push
3. GitHub Pages aktualisiert automatisch (dauert ~1 Minute)
4. **Wichtig**: Nutzer müssen die App neu laden (Seite aktualisieren)

## Eigene Domain (optional)

Falls du eine eigene Domain hast (z.B. `stundenzettel.meinedomain.de`):

1. Erstelle eine Datei `CNAME` im Repository mit dem Inhalt:
   ```
   stundenzettel.meinedomain.de
   ```
2. Bei deinem Domain-Anbieter einen CNAME-Record anlegen:
   ```
   stundenzettel → DEIN-USERNAME.github.io
   ```

## Datenschutz

- Alle Daten bleiben **lokal auf deinem Gerät**
- Nichts wird an Server gesendet
- GitHub Pages hostet nur die App, nicht deine Daten
- Beim Löschen der Browser-Daten werden auch die Stundenzettel gelöscht
- Regelmäßige CSV-Exports als Backup empfohlen!

## Technische Details

- React 18 (UMD-Build)
- Babel Standalone für JSX-Transformation
- Service Worker für Offline-Funktionalität
- IndexedDB-Persistenz über `window.storage`
- Keine externen Abhängigkeiten außer CDN-Libraries

## Support

Bei Problemen:
1. Browser-Cache leeren und neu laden
2. Prüfen ob alle Dateien hochgeladen wurden
3. In GitHub Actions Logs schauen (falls Build fehlschlägt)

---

Viel Erfolg mit deiner Stundenzettel-App! 🎭⏱️
