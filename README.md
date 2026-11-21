# 🏖️ Urlaubsfinanzen

Eine einfache Web-App zur Planung und Verwaltung der Urlaubsfinanzen. Sie zeigt eine Jahresübersicht, aufgeteilt in Monate, mit Einzahlungen, Ausgaben, laufenden Kosten und Prognosen zum Jahresende.

Die App besteht aus **einer einzigen Datei** (`index.html`), benötigt keinen Server und kein Benutzerkonto und läuft auf dem Handy und am Computer.

---

## ✨ Funktionen

### 📊 Übersicht
- **Einzahlungen:** bisher eingezahlt und Prognose zum Jahresende
- **Ausgaben:** alle tatsächlichen Ausgaben (inklusive bereits gebuchter laufender Kosten) und darunter die Prognose zum Jahresende
- **Verfügbar:** aktueller Stand und Prognose zum Jahresende (Einzahlungen − Ausgaben)
- Hinweis auf **anstehende Reisen** in den nächsten 30 Tagen
- Formular zum Erfassen von **Ausgaben** mit Urlaub, Kategorie, Beschreibung, Betrag und Datum
- Block **Urlaubskosten: geschätzt vs. tatsächlich** pro Urlaub mit Fortschrittsbalken
- **Ausgaben nach Kategorie** inklusive laufender Kosten

### 📍 Urlaube
- Reiseziel, Reisebeginn, Reiseende (Format TT.MM.JJJJ) und geschätzte Kosten
- Urlaube lassen sich **bearbeiten** (✏️) und **löschen** (🗑️)
- Pro Urlaub werden geschätzte und tatsächliche Kosten sowie alle zugehörigen Ausgaben angezeigt

### 🗓️ Kalender
- Alle 12 Monate des gewählten Jahres mit Einzahlungen, Ausgaben und Monatssaldo
- Urlaube erscheinen in jedem Monat, den die Reise berührt
- Zukünftige Monate sind als **Geplant** markiert

### 📈 Einzahlungen
- **Automatische monatliche Einzahlung** am 1. des Monats (Standard: 1.300 €, frei anpassbar)
- Schalter **Aktiv/Inaktiv pro Jahr**
- **Zusätzliche Einzahlungen** mit Monat, Betrag und Beschreibung
- Monatsübersicht mit Summe und Prognose

### 🔁 Laufende Kosten
- Wiederkehrende Kosten, zum Beispiel Versicherungen oder Abos
- Intervall: **monatlich, vierteljährlich oder jährlich**
- Beginn und optional Ende
- Buchung jeweils am **1. des Monats**

### 🏷️ Kategorien
Pauschal · Flug · Hotel · Nebenkosten · Verpflegung · Shopping · Aktivitäten · Mietwagen · Benzin · Laufende Kosten

### 💾 Backup & Übertragung
- Export aller Daten als Text, zum Kopieren und Aufbewahren
- Import auf einem anderen Gerät oder in einem anderen Browser

---

## 🧮 So wird gerechnet

| Wert | Berechnung |
|------|-----------|
| Einzahlungen (bisher) | Automatische Einzahlungen bis einschließlich aktuellem Monat + zusätzliche Einzahlungen |
| Ausgaben (tatsächlich) | Erfasste Ausgaben + bereits gebuchte laufende Kosten |
| Verfügbar (aktuell) | Einzahlungen (bisher) − Ausgaben (tatsächlich) |
| Prognose Einzahlungen | 12 × monatliche Einzahlung + zusätzliche Einzahlungen |
| Prognose Ausgaben | Pro Urlaub der höhere Wert aus Schätzung und tatsächlichen Kosten + alle laufenden Kosten des Jahres |
| Prognose Verfügbar | Prognose Einzahlungen − Prognose Ausgaben |

**Hinweise:**
- Ein Urlaub zählt für die Prognose zu dem Jahr, in dem die **Reise beginnt**.
- Zukünftige Monate werden erst gezählt, wenn sie erreicht sind. Bis dahin sind sie als „Geplant“ grau dargestellt.

---

## 🔒 Datenspeicherung und Datenschutz

- Alle Eingaben werden **ausschließlich lokal im Browser** deines Geräts gespeichert (`localStorage`).
- Es werden **keine Daten an einen Server gesendet**.
- Die Daten sind pro Gerät und pro Browser getrennt. Ein anderes Gerät oder ein anderer Browser startet leer.
- Wenn du den Browser-Cache oder die Website-Daten löschst, gehen die Daten verloren. Erstelle deshalb regelmäßig ein **Backup** über „Backup & Übertragung“.
- Die Daten sind nicht verschlüsselt. Schütze dein Gerät mit einer Bildschirmsperre.

---

## 🚀 Veröffentlichen mit GitHub Pages

1. Neues **öffentliches** Repository auf [github.com/new](https://github.com/new) anlegen (neutraler Name, z. B. `haushalt-app`).
2. Datei **`index.html`** erstellen und den Code einfügen, dann **Commit changes**.
3. **Settings → Pages:** Source auf **Deploy from a branch**, Branch **main**, Ordner **/ (root)** und **Save**.
4. Nach 1–2 Minuten ist die App unter `https://DEIN-NAME.github.io/REPOSITORY-NAME/` erreichbar.

> ⚠️ **Sichtbarkeit:** Bei kostenlosen GitHub-Konten ist die veröffentlichte Seite öffentlich. Der Code ist für alle sichtbar, deine eingegebenen Daten bleiben aber nur in deinem Browser. Trage keine persönlichen Daten in den Code oder den Repository-Namen ein.

### Aktualisieren
`index.html` im Repository öffnen, auf das Stift-Symbol tippen, neuen Code einfügen und mit **Commit changes** speichern. Adresse und gespeicherte Daten bleiben unverändert.

---

## 📱 Auf dem Handy nutzen

- **iPhone (Safari):** Teilen-Symbol → „Zum Home-Bildschirm“
- **Android (Chrome):** Menü (⋮) → „Zum Startbildschirm hinzufügen“

Nutze die App immer im **selben Browser** bzw. über dasselbe Home-Bildschirm-Symbol, damit deine Daten erhalten bleiben.

---

## 🛠️ Technik

- Eine einzelne HTML-Datei, kein Build-Prozess
- [React 18](https://react.dev/) und [Babel Standalone](https://babeljs.io/docs/babel-standalone) über cdnjs
- Eigenes CSS, ohne zusätzliche Bibliotheken
- Speicherung im `localStorage`
- Eine Internetverbindung ist nötig, um React beim Start zu laden

---

## 📄 Lizenz

Private Nutzung. Passe die App nach Belieben an deine Bedürfnisse an.
