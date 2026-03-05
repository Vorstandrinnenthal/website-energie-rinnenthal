# Energie Rinnenthal eG – Website Summary & Changelog

> Diese Datei dient als Kontext-Referenz fuer Claude Code, um Aenderungen an der Website
> effizient durchzufuehren und zu dokumentieren. Letzte Aktualisierung: 2026-03-05

---

## Technischer Aufbau

- **Single-Page Application**: Eine einzige `index.html` (ca. 2035 Zeilen)
- **Routing**: Hash-basiert (`#startseite`, `#warum-nahwaerme`, etc.) via JavaScript
- **Styling**: Alles inline in einem `<style>`-Block (Zeilen 35–1082)
- **JavaScript**: Inline am Ende der Datei (Zeilen 1754–2032)
- **Fonts**: Self-hosted woff2 (DM Serif Display, Source Sans 3) im Ordner `fonts/`
- **Kein Build-Tool**: Reines HTML/CSS/JS, kein Framework
- **Git-Repository**: Vorhanden im Ordner
- **Logo**: `logo.png` im Root, Fallback auf friedberg.de URL

### CSS-Variablen (Design-Tokens)
- `--color-primary`: #1A6B35 (Gruen)
- `--color-primary-dark`: #124D26
- `--color-primary-light`: #22884A
- `--color-accent`: #E9A820 (Gold)
- `--color-accent-dark`: #D4941A
- `--color-warm`: #F7F5F0 (Hintergrund-Alt)
- `--color-text`: #1E2A1E
- `--font-display`: DM Serif Display (Ueberschriften)
- `--font-body`: Source Sans 3 (Fliesstext)

---

## Seitenstruktur (Pages)

### 1. Startseite (`#startseite`, Zeilen 1115–1243)
- **Hero**: Logo, Badge "Gegruendet am 9. April 2025", Headline, Subtitle, Stats (95 Mitglieder, 100% Erneuerbar, 0 Gewinnorientierung)
- **Hero-Card**: "Warum Nahwaerme?" mit 5 Bullet-Points
- **Aktuelles (News)**: 3 Karten
  - Nov 2025: Infoveranstaltung im Sportheim BCR
  - Okt 2025: Angebote von regionalen Unternehmen
  - Apr 2025: Gruendung der Energie Rinnenthal eG
- **Vorteile**: 6 Karten (Kostensicherheit, Bestandserhalt, Klimafreundlich, In Buergerhand, Sorglos-Waerme, Wertsteigerung)
- **CTA**: "Jetzt Mitglied werden!"

### 2. Warum Nahwaerme (`#warum-nahwaerme`, Zeilen 1246–1352)
- **Intro-Text**: GEG, CO2-Preise, fossile Brennstoffe
- **Vergleich Hackschnitzel vs. Heizoel**: Zwei Karten mit Preisboxen
  - Hackschnitzel: 3,1–3,7 ct/kWh (Quelle: C.A.R.M.E.N./TFZ Bayern)
  - Heizoel: 9,4–9,5 ct/kWh (Quelle: TFZ Bayern/tecson)
- **CO2-Bepreisung**: Tabelle 2025–2045 (55 EUR/t bis 300 EUR/t)
- **Kostendiagramm**: Canvas-Chart, Heizoel vs. Hackschnitzel 2025–2045
- **Vorteile Genossenschaft**: 6 Karten (Keine Gewinnabsicht, Geringer Invest, Null Wartung, Regional, Wertsteigerung, Gemeinschaft)
- **Beispielrechnung**: EFH 20.000 kWh/Jahr, Heizoel heute ~1.900 EUR vs. 2040 ~3.800 EUR, Nahwaerme 1.000–1.400 EUR
- **CTA**: "Jetzt umsteigen"

### 3. Mitglied werden (`#mitglied-werden`, Zeilen 1355–1419)
- **5-Schritte-Prozess** (vertikale Timeline):
  1. Kontakt zum Vorstand (Vorstand@energie-rinnenthal.de)
  2. Erhebungsbogen ausfuellen (PDF Download)
  3. Beitrittserklärung einreichen (DOCX Download)
  4. Geschaeftsanteil einzahlen
  5. Liefer- und Leistungsvertrag unterschreiben
- **CTA**: "Fragen zum Beitritt?"

### 4. Ueber uns (`#ueber-uns`, Zeilen 1422–1529)
- **Intro**: Beschreibung der Genossenschaft, Zusammenarbeit mit Enerpipe
- **Statistik-Box**: 95 Mitglieder, Gruendung 9. April 2025
- **Projekt-Timeline** (horizontal, 4 Schritte):
  - [DONE] Gruendung (April 2025)
  - [DONE] Planung & Erhebung (Sommer 2025)
  - [ACTIVE] Foerderung & Vergabe (Winter 2025/26)
  - [FUTURE] Baubeginn (Q3 2026)
- **Vorstand**: Dr. Jochen Schneider, Christian Treffler, Simon Pletschacher
- **Aufsichtsrat**: Matthias Stegmeir (Vorsitz), Manfred Bradl (Stv.), Roland Eichmann (1. Buergermeister), Josef Fischer, Dominik Kreitmair
- **Arbeitsgruppe**: 12 Mitglieder aufgelistet
- **Mitglieder-Hinweis**: 95 Mitglieder, Beitritt weiterhin moeglich

### 5. Dokumente (`#dokumente`, Zeilen 1532–1615)
- **Akkordeon mit 4 Kategorien**:
  - Genossenschaft (5 Dokumente): Satzung (PDF), Erhebungsbogen (PDF), Beitrittserklaerung (DOCX), Vollmacht (DOCX), Uebertragung Geschaeftsanteil (DOCX)
  - Nahwaermenetz (4 Dokumente): FAQ Nahwaerme (PDF), Trassenplan (PDF), Kickoff Enerpipe (PDF), Heizungsfoerderung Brandl (PDF)
  - Praesentationen (2 Dokumente): Infoveranstaltung 10.11.2025 (PDF), 1. Generalversammlung (PPTX)
  - Infobriefe (3 Dokumente): Dez 2025 (PDF), Maerz 2025 (PDF), Dez 2024 (PDF)

### 6. FAQ (`#faq`, Zeilen 1618–1637)
- **7 Fragen** (Akkordeon):
  1. Was ist eine Buergerenergiegenossenschaft?
  2. Wie funktioniert ein Nahwaermenetz mit Hackschnitzeln?
  3. Kann ich meine bestehenden Heizkoerper weiter nutzen?
  4. Wer entscheidet ueber die Waermepreise?
  5. Kann ich jetzt noch Mitglied werden?
  6. Wer plant und baut das Nahwaermenetz?
  7. Gibt es staatliche Foerderungen?

### 7. Kontakt (`#kontakt`, Zeilen 1640–1662)
- **Adresse**: Energie Rinnenthal eG, Aretinstrasse 25, 86316 Friedberg
- **E-Mail**: Vorstand@energie-rinnenthal.de

### 8. Impressum (`#impressum`, Zeilen 1665–1694)
- Angaben gemaess § 5 DDG
- Registernummer: GnR 1753 (AG Augsburg)
- Pruefungsverband: GVB Muenchen

### 9. Datenschutz (`#datenschutz`, Zeilen 1697–1716)
- Verantwortlicher, Server-Logfiles, Schriftarten (lokal gehostet), Rechte

### Footer (Zeilen 1720–1752)
- Logo, Beschreibung, Navigation, externe Links (friedberg.de), Impressum/Datenschutz

---

## Dateien im Ordner `/home/simon/nahwaerme-website/`

```
index.html                    – Hauptdatei (gesamte Website)
logo.png                      – Logo (mit Fallback-URL)
fonts/
  dm-serif-display-latin.woff2    – DM Serif Display (latin)
  dm-serif-display-latin-ext.woff2 – DM Serif Display (latin-ext)
  source-sans-3-latin.woff2       – Source Sans 3 Variable (latin)
  source-sans-3-latin-ext.woff2   – Source Sans 3 Variable (latin-ext)
docs/
  genossenschaft/
    satzung-energie-rinnenthal-eg.pdf
    satzung-energie-rinnenthal-eg.docx
    erhebungsbogen.pdf
    beitrittserklaerung.docx
    vollmacht-beitritt.docx
    uebertragung-geschaeftsanteil.docx
  nahwaermenetz/
    fragen-antworten-nahwaerme.pdf
    trassenplan-nahwaermenetz.pdf
    kickoff-enerpipe.pdf
    heizungsfoerderung-brandl.pdf
  praesentationen/
    infoveranstaltung-2025-11-10.pdf
    praesentation-1-generalversammlung.pptx
  infobriefe/
    infobrief-2025-12.pdf
    infobrief-2025-03.pdf
    infobrief-2024-12.pdf
```

---

## Wichtige Kennzahlen (aktuell auf der Website)

| Kennzahl | Wert | Stelle |
|----------|------|--------|
| Mitglieder | 95 | Hero-Stats (Z.1129), About-Visual (Z.1438), Mitglieder-Hinweis (Z.1525), Timeline (Z.1454) |
| Gruendungsdatum | 9. April 2025 | Hero-Badge (Z.1123), About (Z.1440), Timeline (Z.1454) |
| Hackschnitzel-Preis | 3,1–3,7 ct/kWh | Warum-Nahwaerme Preisbox (Z.1267) |
| Heizoel-Preis | 9,4–9,5 ct/kWh | Warum-Nahwaerme Preisbox (Z.1278) |
| Kontakt-E-Mail | Vorstand@energie-rinnenthal.de | Mehrfach |
| Adresse | Aretinstrasse 25, 86316 Friedberg | Kontakt, Impressum |
| Registernummer | GnR 1753 | Impressum (Z.1682) |
| Projekt-Phase aktuell | Foerderung & Vergabe (Winter 2025/26) | Timeline (Z.1467) |
| Naechster Meilenstein | Baubeginn Q3 2026 | Timeline (Z.1476) |

---

## Changelog

### 2026-03-05 – Runde 5: Font Self-Hosting, Accordion-Fix, Inline-Styles

**DSGVO/GDPR-Fix – Google Fonts Self-Hosting:**
- Google Fonts CDN komplett entfernt (preconnect + stylesheet Link)
- 4 woff2-Dateien lokal gehostet in `fonts/` (DM Serif Display latin + latin-ext, Source Sans 3 Variable latin + latin-ext)
- @font-face Deklarationen im `<head>` mit unicode-range (nur latin + latin-ext fuer Deutschland)
- Source Sans 3 als Variable Font (weight 200-900 in einer Datei pro Subset)
- Datenschutz-Section aktualisiert: "Schriftarten lokal gehostet, keine Verbindung zu Google-Servern"

**Accordion-Konsistenz:**
- Dokumente-Akkordeon: CSS `max-height: 600px` entfernt (konnte Inhalt abschneiden)
- Stattdessen JS `scrollHeight` wie bei FAQ (dynamische Hoehe)
- Inline `onclick` Handler durch `data-docs-toggle` Attribut + Event Listener ersetzt
- Gemeinsame `toggleAccordion()` Hilfsfunktion fuer beide Akkordeons
- Initial geoeffnete Kategorie ("Genossenschaft") wird per JS korrekt initialisiert

**Inline-Styles entfernt (alle ~30 Vorkommen):**
- Neue CSS-Klassen: `.link-primary`, `.text-source`, `.hero-cta-wrap`, `.explainer-section`, `.explainer-text`, `.explainer-link`
- CO2-Preiskarten: `.co2-price-low`, `.co2-price-mid`, `.co2-price-high`, `.co2-price-max`
- Beispielrechnung: `.amount-gold`, `.amount-red`
- Mitglied-werden Statistikbox: `.member-stats-box`, `.member-stats-number`, `.member-stats-label`, `.member-stats-note`
- Timeline-Intro: `.timeline-intro-title`, `.timeline-intro-text`
- Kontakt-Section: `.contact-text`, `.contact-links`
- Canvas: `.chart-canvas`
- 0 inline `style=` Attribute verbleiben im HTML

### 2026-03-05 – Grosse SEO & UX Ueberarbeitung (4 Runden)

**Runde 1 – SEO Grundlagen:**
- `robots.txt` erstellt mit Sitemap-Referenz
- `sitemap.xml` erstellt (alle Seiten + wichtige PDFs)
- `logo.png` heruntergeladen (fehlte lokal), `favicon.ico` + `logo-192.png` erstellt
- Canonical URL, `og:url`, `og:image`, `og:site_name` hinzugefuegt
- Twitter Card Meta Tags hinzugefuegt
- Geo Meta Tags (DE-BY, Friedberg) hinzugefuegt
- Keywords Meta Tag hinzugefuegt
- Meta Description erweitert mit "Heizkosten senken", "klimafreundlich"
- Schema.org erweitert: LocalBusiness, GeoCoordinates, areaServed, logo, sameAs
- FAQPage Schema fuer alle FAQ-Eintraege (Google Rich Snippets)

**Runde 2 – UX & Accessibility:**
- CTA-Button in Hero-Section hinzugefuegt ("So werde ich Mitglied")
- Skip-to-Content Link fuer Screenreader/Tastaturnutzer
- Farbkontrast verbessert (Hero-Text opacity 0.7→0.85, 0.85→0.9)
- Mobile Menu Transition repariert (display:none→opacity/pointer-events)
- `text-wrap: balance` fuer Ueberschriften
- Print-Stylesheet hinzugefuegt
- Footer Touch-Targets verbessert (min 44px)
- "Platzhalter-Bilder" Text entfernt (Vorstand-Section)
- "Mitglied werden" zum Footer hinzugefuegt
- Dead CSS (.downloads-grid) entfernt

**Runde 3 – SEO Content:**
- Hero Subtitle: "Heizkosten senken", "Friedberg (Bayern)" integriert
- Neue Section "So funktioniert Nahwaerme" auf Startseite (Fernwaerme, Waermepumpe-Vergleich, GEG)
- H2-Ueberschriften optimiert mit Keywords auf allen Seiten
- 2 neue FAQ-Eintraege: "Was kostet Nahwaerme?" + "Nahwaerme vs. Waermepumpe"
- FAQPage Schema aktualisiert (jetzt 9 Eintraege)
- Interne Links in FAQ-Antworten (#mitglied-werden, #dokumente, #warum-nahwaerme)
- Social-Proof Counter (95 Mitglieder) auf Mitglied-werden Seite
- Kontaktseite erweitert: 3. Karte (Lage), Cross-Links, Kontext-Text
- Vorausgefuellte mailto-Betreffzeile
- Lokaler Kontext in Ueber-uns (Aichach-Friedberg, Bayerisch-Schwaben)

**Runde 4 – Accessibility & Content:**
- Focus-Management bei Seitennavigation (Heading wird fokussiert)
- aria-hidden Toggling auf Page-Containern
- Fallback auf Startseite bei ungueltigem Hash
- Escape-Taste schliesst Mobile Menu
- document.write() durch DOM-Manipulation ersetzt
- Resize-Handler debounced (150ms)
- apple-touch-icon Meta Tag
- width/height Attribute auf Logo-Bildern (CLS)
- News-Karte fuer Maerz 2026 (Foerderantraege, Vergabe)
- Enerpipe mit Link zur Website versehen

### 2026-03-03 – Roland Eichmann Rolle aktualisiert
- Aufsichtsrat (Z.1500): Rolle von Roland Eichmann von "1. Bürgermeister" zu "Mitglied" geaendert
- Arbeitsgruppe (Z.1507): "Roland Eichmann (1. Bürgermeister)" zu "Roland Eichmann (Mitglied)" geaendert

### 2026-03-03 – Aenderungen aus Mails (Jochen Schneider + Simon)
- Schritt 3 "Beitrittserklärung": Text geaendert — Vollmacht-Satz entfernt, neuer Text "Nach positivem Feedback durch den Vorstand sind Sie Mitglied"
- Schritt 5 "LLV": Text erweitert — LLV kommt vom Vorstand, Hinweis auf Foerderung und Energieberater
- E-Mail korrigiert: `Vorstand@energie-rinnenthal.de` → `Vorstand@energie-rinnenthal.de` (alle Vorkommen inkl. Schema.org)
- Arbeitsgruppe: "Inn Lindemeyer" → "Inno Lindemeyer"
- Arbeitsgruppe: Matthias Bissinger und Josef Seitz jr. entfernt (jetzt 12 statt 14 Mitglieder)

### 2026-03-03 – Initiale Dokumentation
- Summary-Datei erstellt basierend auf aktuellem Stand der Website

---

*Fuer jede Aenderung bitte einen neuen Eintrag im Changelog mit Datum, Beschreibung und betroffenen Zeilen/Sektionen anlegen.*
