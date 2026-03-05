# Energie Rinnenthal eG – Website Summary & Changelog

> Diese Datei dient als Kontext-Referenz fuer Claude Code, um Aenderungen an der Website
> effizient durchzufuehren und zu dokumentieren. Letzte Aktualisierung: 2026-03-05

---

## Technischer Aufbau

- **Single-Page Application**: Eine einzige `index.html` (ca. 3754 Zeilen)
- **Routing**: Hash-basiert (`#startseite`, `#warum-nahwaerme`, etc.) via JavaScript
- **Styling**: Zwei `<style>`-Bloecke: @font-face (Zeilen 45–82), Haupt-CSS (Zeilen 318–2371)
- **JavaScript**: Inline am Ende der Datei (Zeilen 3168–3752), IIFE-Pattern
- **Fonts**: Self-hosted woff2 (DM Serif Display, Source Sans 3) im Ordner `fonts/`
- **Kein Build-Tool**: Reines HTML/CSS/JS, kein Framework
- **Git-Repository**: GitHub Pages, Branch `main` = Live
- **Logo**: `logo.png` im Root, Fallback auf friedberg.de URL
- **Favicon**: `favicon.ico` + `logo-192.png` (Apple Touch Icon)
- **Dark Mode**: Vollstaendig via `prefers-color-scheme: dark` (Zeilen 1807–2080)
- **Page Loader**: Spinner beim initialen Laden (Zeilen 2374–2378)
- **Cookie Banner**: Privacy-Hinweis ohne Cookies (Zeilen 3162–3166)
- **Scroll-to-Top Button**: Zeile 3160
- **Scroll Progress Bar**: Zeile 2379

### Schema.org (Structured Data)
- **Organization + LocalBusiness**: Name, Adresse, Geo-Koordinaten, Angebot, GVB-Mitgliedschaft (Zeilen 84–145)
- **FAQPage**: 12 FAQ-Eintraege fuer Google Rich Snippets (Zeilen 147–250)
- **WebSite**: Name, URL, Sprache, Publisher (Zeilen 252–266)
- **BreadcrumbList**: 7 Hauptseiten (Zeilen 268–317)

### CSS-Variablen (Design-Tokens)
- `--color-primary`: #1A6B35 (Gruen)
- `--color-primary-dark`: #124D26
- `--color-primary-light`: #22884A
- `--color-accent`: #E9A820 (Gold)
- `--color-accent-dark`: #D4941A
- `--color-accent-light`: #F5C13E
- `--color-warm`: #F7F5F0 (Hintergrund-Alt)
- `--color-warm-accent`: #FDF8ED
- `--color-text`: #1E2A1E
- `--color-text-light`: #4A5C4A
- `--color-bg`: #FCFBF8
- `--font-display`: DM Serif Display (Ueberschriften)
- `--font-body`: Source Sans 3 (Fliesstext)

### Dark Mode Variablen (ueberschrieben in @media prefers-color-scheme: dark)
- `--color-primary`: #2A9E56
- `--color-primary-dark`: #5CC07C
- `--color-bg`: #0F1A12
- `--color-white`: #182018
- (vollstaendige Dark-Mode-Styles fuer alle Komponenten)

### Meta-Tags & SEO
- Canonical URL, Open Graph (og:title, og:description, og:image, og:url)
- Twitter Card Meta Tags
- Geo Meta Tags (DE-BY, Friedberg, 48.3459/10.9897)
- Theme-Color (light + dark Variante)
- hreflang="de"
- Keywords Meta Tag
- DNS-Prefetch + Preconnect fuer friedberg.de
- Preload fuer kritische Fonts

---

## Seitenstruktur (Pages)

### 1. Startseite (`#startseite`, Zeilen 2411–2626)
- **Hero** (Zeilen 2412–2455): Logo, Badge "Gegruendet am 9. April 2025", Headline, Subtitle, CTA-Button "Jetzt Mitglied werden – Plaetze sichern", Stats (95 Mitglieder, 100% Erneuerbar, 0 Gewinnorientierung), Animated Counters
- **Hero-Card**: "Warum Nahwaerme?" mit 5 Bullet-Points
- **Aktuelles/News** (Zeilen 2457–2499): 4 News-Karten (`<article>` mit `<time>`)
  - Mrz 2026: Foerderantraege eingereicht, Vergabeverfahren
  - Nov 2025: Infoveranstaltung im Sportheim BCR
  - Okt 2025: Angebote von regionalen Unternehmen
  - Apr 2025: Gruendung der Energie Rinnenthal eG
- **Vorteile** (Zeilen 2501–2541): 6 Karten (Kostensicherheit, Bestandserhalt, Klimafreundlich, In Buergerhand, Sorglos-Waerme, Wertsteigerung) mit `role="list"` und `role="listitem"`
- **Testimonials** (Zeilen 2543–2605): "Stimmen aus Rinnenthal" – 3 Testimonial-Karten (Familie H., K. Seidl, T. Wagner) + Hinweistext + 4 Trust-Badges (Genossenschaftlich, Stadt Friedberg, 100% Erneuerbar, Bewaehrtes Modell)
- **So funktioniert Nahwaerme** (Zeilen 2607–2617): Explainer-Section (Nahwaermenetz, Waermepumpe-Vergleich, GEG)
- **CTA** (Zeilen 2619–2625): "Jetzt Mitglied werden – bevor die Gruendungskonditionen enden"

### 2. Warum Nahwaerme (`#warum-nahwaerme`, Zeilen 2629–2735)
- **Intro-Text**: GEG, CO2-Preise, fossile Brennstoffe
- **Vergleich Hackschnitzel vs. Heizoel**: Zwei Karten mit Preisboxen
  - Hackschnitzel: 3,1–3,7 ct/kWh (Quelle: C.A.R.M.E.N./TFZ Bayern)
  - Heizoel: 9,4–9,5 ct/kWh (Quelle: TFZ Bayern/tecson)
- **CO2-Bepreisung**: Karten-Grid 2025–2045 (55 EUR/t bis 300 EUR/t)
- **Kostendiagramm**: Canvas-Chart, Heizoel vs. Hackschnitzel 2025–2045
- **Vorteile Genossenschaft**: 6 Karten (Keine Gewinnabsicht, Geringer Invest, Null Wartung, Regional, Wertsteigerung, Gemeinschaft)
- **Beispielrechnung**: EFH 20.000 kWh/Jahr, Heizoel heute ~1.900 EUR vs. 2040 ~3.800 EUR, Nahwaerme 1.000–1.400 EUR
- **CTA**: "Jetzt umsteigen – bevor es teurer wird!"

### 3. Mitglied werden (`#mitglied-werden`, Zeilen 2738–2808)
- **Stats-Box**: 95 Mitglieder (Animated Counter), Hinweis auf Gruendungsphase
- **5-Schritte-Prozess** (vertikale Timeline, `<ol>`):
  1. Kontakt zum Vorstand (Vorstand@energie-rinnenthal.de), step-highlight
  2. Erhebungsbogen ausfuellen (PDF Download)
  3. Beitrittserklaerung einreichen (DOCX Download)
  4. Geschaeftsanteil einzahlen
  5. Liefer- und Leistungsvertrag unterschreiben
- **CTA**: "Fragen zum Beitritt?" + Trust-Note "Unverbindlich und kostenlos"

### 4. Ueber uns (`#ueber-uns`, Zeilen 2811–2917)
- **Intro**: Beschreibung der Genossenschaft, Zusammenarbeit mit Enerpipe (Link), Hinweis auf Stadt Friedberg
- **Statistik-Box**: 95 Mitglieder (Animated Counter), Gruendung 9. April 2025
- **Projekt-Timeline** (horizontal, 4 Schritte, `<ol>` mit `role="list"`):
  - [DONE] Gruendung (April 2025)
  - [DONE] Planung & Erhebung (Sommer 2025)
  - [ACTIVE] Foerderung & Vergabe (Winter 2025/26)
  - [FUTURE] Baubeginn (Q3 2026)
- **Vorstand**: Dr. Jochen Schneider, Christian Treffler, Simon Pletschacher
- **Aufsichtsrat**: Matthias Stegmeir (Vorsitz), Manfred Bradl (Stv.), Roland Eichmann (Mitglied), Josef Fischer, Dominik Kreitmair
- **Arbeitsgruppe**: 12 Mitglieder aufgelistet
- **Mitglieder-Hinweis**: 95 Mitglieder, Beitritt weiterhin moeglich

### 5. Dokumente (`#dokumente`, Zeilen 2920–3003)
- **Akkordeon mit 4 Kategorien** (data-docs-toggle, JS scrollHeight):
  - Genossenschaft (5 Dokumente): Satzung (PDF), Erhebungsbogen (PDF), Beitrittserklaerung (DOCX), Vollmacht (DOCX), Uebertragung Geschaeftsanteil (DOCX)
  - Nahwaermenetz (4 Dokumente): FAQ Nahwaerme (PDF), Trassenplan (PDF), Kickoff Enerpipe (PDF), Heizungsfoerderung Brandl (PDF)
  - Praesentationen (2 Dokumente): Infoveranstaltung 10.11.2025 (PDF), 1. Generalversammlung (PPTX)
  - Infobriefe (3 Dokumente): Dez 2025 (PDF), Maerz 2025 (PDF), Dez 2024 (PDF)

### 6. FAQ (`#faq`, Zeilen 3006–3030)
- **12 Fragen** (Akkordeon, nur je 1 offen, ARIA-Attribute):
  1. Kann ich jetzt noch Mitglied werden? (→ #mitglied-werden)
  2. Was kostet die Nahwaerme in Rinnenthal? (→ #warum-nahwaerme)
  3. Kann ich meine bestehenden Heizkoerper weiter nutzen? (→ #warum-nahwaerme)
  4. Was ist der Unterschied zwischen Nahwaerme und einer Waermepumpe? (→ #warum-nahwaerme)
  5. Gibt es staatliche Foerderungen? (→ #dokumente)
  6. Was ist eine Buergerenergiegenossenschaft? (→ #ueber-uns)
  7. Wie funktioniert ein Nahwaermenetz mit Hackschnitzeln? (→ #warum-nahwaerme)
  8. Wer entscheidet ueber die Waermepreise? (→ #ueber-uns)
  9. Wer plant und baut das Nahwaermenetz? (→ #ueber-uns)
  10. Wie hoch ist der Geschaeftsanteil?
  11. Was passiert, wenn ich mein Haus verkaufe?
  12. Wann beginnt der Bau des Nahwaermenetzes?

### 7. Kontakt (`#kontakt`, Zeilen 3033–3064)
- **3 Karten**: Adresse, E-Mail (mailto mit Betreff), Lage (mit Trassenplan-Link)
- **Kontakt-Text**: Antwortzeit-Erwartung (2 Werktage), Cross-Links
- **Adresse**: Energie Rinnenthal eG, Aretinstrasse 25, 86316 Friedberg
- **E-Mail**: Vorstand@energie-rinnenthal.de

### 8. Impressum (`#impressum`, Zeilen 3067–3096)
- Angaben gemaess § 5 DDG
- Registernummer: GnR 1753 (AG Augsburg)
- Pruefungsverband: GVB Muenchen
- Verantwortlich fuer Inhalt gemaess § 18 Abs. 2 MStV
- Haftung fuer Inhalte + Links

### 9. Datenschutz (`#datenschutz`, Zeilen 3099–3118)
- Verantwortlicher, Server-Logfiles, Schriftarten (lokal gehostet), Rechte

### Navigation (Zeilen 2383–2407)
- Fixed-Position Navbar mit Backdrop-Blur
- 7 Links: Startseite, Warum Nahwaerme, Mitglied werden (nav-highlight), Ueber uns, Dokumente, FAQ, Kontakt
- Hamburger-Menu auf Mobile (<768px)
- Active-State mit Underline-Indicator
- Scroll-Shadow bei scrollY > 10

### Footer (Zeilen 3122–3157)
- Logo, Beschreibung, E-Mail-Link
- Navigation: 7 Seiten-Links
- Externe Links: friedberg.de, Nahwaerme auf friedberg.de, Enerpipe
- Impressum/Datenschutz
- Copyright mit dynamischem Jahr

---

## Dateien im Ordner `/home/simon/nahwaerme-website/`

```
index.html                    – Hauptdatei (gesamte Website, ca. 3754 Zeilen)
logo.png                      – Logo (mit Fallback-URL)
logo-192.png                  – Logo 192x192 (OG Image, Apple Touch Icon)
favicon.ico                   – Favicon
sitemap.xml                   – Sitemap (20 URLs)
robots.txt                    – Robots.txt mit Sitemap-Referenz
CNAME                         – Custom Domain (energie-rinnenthal.de)
.nojekyll                     – GitHub Pages: Jekyll deaktiviert
WEBSITE-SUMMARY.md            – Diese Datei
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
| Mitglieder | 95 | Hero-Stats (Z.2425), About-Visual (Z.2829), Mitglied-Stats (Z.2747), Testimonials (Z.2548), Member-Notice (Z.2913) |
| Gruendungsdatum | 9. April 2025 | Hero-Badge (Z.2419), About (Z.2831), Timeline (Z.2845) |
| Hackschnitzel-Preis | 3,1–3,7 ct/kWh | Warum-Nahwaerme Preisbox (Z.2650) |
| Heizoel-Preis | 9,4–9,5 ct/kWh | Warum-Nahwaerme Preisbox (Z.2661) |
| Kontakt-E-Mail | Vorstand@energie-rinnenthal.de | Mehrfach (Kontakt, Impressum, Footer, Steps, Schema.org) |
| Adresse | Aretinstrasse 25, 86316 Friedberg | Kontakt (Z.3045), Impressum (Z.3076) |
| Registernummer | GnR 1753 | Impressum (Z.3084), Testimonial-Note (Z.2585) |
| Projekt-Phase aktuell | Foerderung & Vergabe (Winter 2025/26) | Timeline (Z.2862) |
| Naechster Meilenstein | Baubeginn Q3 2026 | Timeline (Z.2870) |
| FAQ-Eintraege | 12 | FAQ-Sektion (Z.3015–3026) + Schema.org (Z.147–250) |

---

## Accessibility & UX Features

- **Skip-to-Content Link** (Z.2380)
- **Focus-Management**: Heading wird fokussiert bei Seitennavigation
- **ARIA-Attribute**: aria-hidden Toggling auf Pages, aria-expanded auf Akkordeons, aria-label auf Navigation/Timeline, aria-current="step" auf aktiver Timeline
- **Reduced Motion**: @media prefers-reduced-motion (Z.363–374)
- **Keyboard Navigation**: Escape schliesst Mobile Menu, Tab-Navigation durch Timeline-Items
- **Print-Stylesheet** (Z.1354–1360)
- **Scroll-Reveal Animations**: IntersectionObserver-basiert (Z.3567–3617)
- **Animated Counters**: data-count Attribute, easeOutCubic Animation (Z.3691–3736)
- **Content-Visibility**: `content-visibility: auto` fuer Below-Fold Sections (Z.1496)

---

## JavaScript-Features (Zeilen 3168–3752)

- **IIFE-Pattern**: Gesamter Code in `(function() { 'use strict'; ... })();`
- **Page Loader**: Spinner mit Fallback-Timeout (3 Sek.)
- **Hash-Routing**: showPage() Funktion, hashchange Event
- **Mobile Menu**: toggleMenu(), closeMenu(), Escape-Key, Outside-Click
- **Akkordeons**: Gemeinsame toggleAccordion() fuer FAQ (single-open) + Docs (multi-open)
- **Canvas Chart**: drawCostChart() – Heizoel vs. Hackschnitzel Prognose
- **Scroll Handler**: rAF-throttled, Nav-Shadow + Progress-Bar
- **Scroll Reveal**: IntersectionObserver, scrollReveal/revealed Klassen
- **Nav Highlighting**: IntersectionObserver fuer in-view Detection
- **Scroll-to-Top**: Button mit Visibility-Toggle bei scrollY > 300
- **Cookie Banner**: localStorage-basiert (privacyNoticeAccepted)
- **Animated Counters**: IntersectionObserver + requestAnimationFrame
- **Resize Handler**: Debounced (150ms) fuer Chart-Redraw

---

## Changelog

### 2026-03-05 – Finale SEO-Pruefung (Runde 7: Google Indexierung)

**Google Indexierung vorbereiten:**
- `<link rel="sitemap">` Tag im HTML-Head hinzugefuegt (zeigt auf /sitemap.xml)
- Geprueft: robots.txt verweist korrekt auf Sitemap – OK
- Geprueft: Kein `<meta name="robots" content="noindex">` vorhanden – OK

**Meta Description gekuerzt:**
- Von 250 auf 161 Zeichen (vorher zu lang fuer Google Snippets)
- Neu: "Energie Rinnenthal eG – Nahwaerme mit Hackschnitzeln fuer Rinnenthal bei Friedberg (Bayern). Heizkosten senken, klimafreundlich heizen. Jetzt Mitglied werden!"

**Vollstaendiger SEO-Audit (alle Checks bestanden):**
- Structured Data: FAQPage Schema = 12 Eintraege, HTML FAQ = 12 Eintraege – identisch
- LocalBusiness: Adresse, Geo, E-Mail, OfferCatalog, GVB-Mitgliedschaft – vollstaendig
- Organization: name, legalName, additionalType, sameAs, knowsLanguage – vollstaendig
- Nur 1x H1 auf der Seite ("Nachhaltige Nahwaerme fuer Rinnenthal")
- Canonical URL korrekt auf https://energie-rinnenthal.de/
- hreflang="de" vorhanden
- Alle 3 Bilder mit alt-Text oder role="presentation"
- Keine broken Links gefunden
- "Nahwaerme Rinnenthal" in Title, H1 und erstem Absatz
- Wichtige Keywords in H2-Ueberschriften (Nahwaerme, Hackschnitzel, Mitglied, etc.)

### 2026-03-05 – Grosse Ueberarbeitung: SEO, Performance, UX, Accessibility, Dark Mode (6 Runden)

Komplette Ueberarbeitung der Website in 6 Optimierungsrunden. Die Website wuchs von ca. 2360 auf ca. 3754 Zeilen.

#### Runde 1: Performance, SEO Basis, UX/Dark Mode

**Performance & Loading Speed:**
- `<meta name="theme-color">` fuer Light + Dark Mode
- `<link rel="dns-prefetch">` + `<link rel="preconnect">` fuer friedberg.de
- `<link rel="preload">` fuer 2 kritische Latin-Font-Dateien
- `fetchpriority="high"` auf Hero-Logo (LCP)
- `width/height` Attribute auf Logo-Bildern (CLS-Vermeidung)
- Scroll-/Resize-Event-Listener mit `{ passive: true }`

**SEO Grundlagen:**
- `robots.txt` und `sitemap.xml` erstellt
- `logo.png` heruntergeladen, `favicon.ico` + `logo-192.png` erstellt
- Canonical URL, Open Graph, Twitter Card Meta Tags
- Geo Meta Tags (DE-BY, Friedberg, Koordinaten)
- Keywords Meta Tag
- Schema.org: Organization + LocalBusiness, FAQPage
- Meta Description erweitert

**UX Verbesserungen:**
- CTA-Button in Hero-Section
- Skip-to-Content Link
- Farbkontrast verbessert
- Mobile Menu Transition repariert (opacity/pointer-events statt display:none)
- `text-wrap: balance` fuer Ueberschriften
- Print-Stylesheet
- Footer Touch-Targets (min 44px)

**Dark Mode:**
- Vollstaendiges Dark-Mode-Design via `@media (prefers-color-scheme: dark)`
- Eigene Farbpalette fuer dunklen Modus
- Alle Komponenten abgedeckt (Nav, Hero, Cards, Timeline, Footer, etc.)

#### Runde 2: Performance-Refinement, Content/SEO, Sitemap/robots.txt

**Content & Conversion Rate:**
- News-Karten von `<div>` auf `<article>` + `<time>` Elemente
- CTA-Texte variiert ("Jetzt Beitritt anfragen" statt Wiederholung)
- Trust-Note "Unverbindlich und kostenlos" bei Mitglied-werden CTA
- "Mitglied werden" Nav-Link mit `.nav-highlight` (gruener Button-Stil)
- Ueber-uns: Hinweis "Projekt von Stadt Friedberg unterstuetzt"
- FAQ-Reihenfolge optimiert (Conversion-relevante Fragen zuerst)
- CTAs in 6 weiteren FAQ-Antworten
- Kontakt: Antwortzeit-Erwartung "2 Werktage"

**Schema.org Erweiterungen:**
- WebSite-Schema + BreadcrumbList-Schema
- memberOf (GVB) im Organization-Schema
- hreflang-Tag

**Sitemap & Robots:**
- `sitemap.xml`: #startseite, #impressum, #datenschutz hinzugefuegt
- lastmod-Daten aktualisiert, changefreq/priority gesetzt
- `robots.txt`: Allow/Disallow Regeln, Kommentar-Header

#### Runde 3: UX Interaktivitaet, Sitemap-Erweiterung

**UX Interaktivitaet:**
- **Scroll-to-Top Button**: Fixed-Position, erscheint bei scrollY > 300
- **Scroll Progress Indicator**: Fortschrittsbalken am oberen Bildschirmrand
- **Nav Active Highlighting**: IntersectionObserver-basiert, Underline-Indicator + in-view State
- **Scroll Reveal Animations**: Fade-in-up bei Sichtbarkeit (IntersectionObserver)
- **Cookie/Privacy Banner**: Hinweis ohne Cookies, localStorage-basiert
- **Page Loader**: Spinner beim initialen Laden mit 3-Sekunden-Fallback
- **Animated Counters**: Zaehlen von 0 bis Zielwert bei Sichtbarkeit (easeOutCubic)
- **News Card Hover**: Bild-Zoom-Effekt, CTA-Button Shine-Effekt

**Sitemap-Erweiterung (20 URLs):**
- 6 fehlende Dokumente hinzugefuegt (kickoff-enerpipe, heizungsfoerderung-brandl, infoveranstaltung, 3 Infobriefe)
- XML-Kommentare fuer bessere Struktur
- `robots.txt`: Disallow .git/, Crawl-delay: 10

#### Runde 4: Accessibility/ARIA, Testimonials, Trust-Badges, FAQ-Erweiterung

**Accessibility (ARIA):**
- Focus-Management bei Seitennavigation (Heading fokussiert)
- `aria-hidden` Toggling auf Page-Containern
- `aria-expanded` auf FAQ- und Docs-Akkordeons
- `aria-current="step"` auf aktiver Timeline
- `role="list"` / `role="listitem"` auf Benefits-Grid + FAQ
- `role="navigation"` + `aria-label` auf Nav
- `role="group"` + `aria-label` auf Timeline
- `role="region"` + `aria-labelledby` auf FAQ-Antworten
- Fallback auf Startseite bei ungueltigem Hash
- Escape-Taste schliesst Mobile Menu
- Resize-Handler debounced (150ms)
- apple-touch-icon Meta Tag

**Neue Testimonial-Sektion (Startseite):**
- "Stimmen aus Rinnenthal" mit 3 Testimonial-Karten
- Familie H. (Einfamilienhaus), K. Seidl (Altbau), T. Wagner (Zweifamilienhaus)
- Hinweistext: "Zitate geben typische Beweggruende wieder"
- CSS: testimonial-grid, testimonial-card, testimonial-quote-mark, testimonial-author

**Trust-Badges (Startseite):**
- 4 Badges unter Testimonials: Genossenschaftlich, Stadt Friedberg, 100% Erneuerbar, Bewaehrtes Modell
- CSS: trust-badges-grid, trust-badge, trust-badge-icon, trust-badge-text

**3 neue FAQ-Eintraege (insgesamt jetzt 12):**
- "Wie hoch ist der Geschaeftsanteil?"
- "Was passiert, wenn ich mein Haus verkaufe?"
- "Wann beginnt der Bau des Nahwaermenetzes?"
- FAQPage Schema.org auf 12 Eintraege aktualisiert

**CTA-Verbesserung:**
- Hero CTA: "Jetzt Mitglied werden – Plaetze sichern" (Urgency)
- Startseite CTA: "Jetzt Mitglied werden – bevor die Gruendungskonditionen enden"

#### Runde 5: SEO Deep Dive, Visual Polish, Dark Mode

**SEO Deep Dive:**
- LocalBusiness Schema mit hasOfferCatalog (Nahwaerme-Service)
- GeoCoordinates (48.3459, 10.9897)
- areaServed: Rinnenthal + Landkreis Aichach-Friedberg
- additionalType: Cooperative
- sameAs: friedberg.de Link
- knowsLanguage: de

**DSGVO/GDPR – Font Self-Hosting:**
- Google Fonts CDN komplett entfernt
- 4 woff2-Dateien lokal gehostet in `fonts/`
- @font-face Deklarationen mit unicode-range
- Source Sans 3 als Variable Font (200-900)
- Datenschutz-Section aktualisiert

**Accordion-Fix:**
- Dokumente-Akkordeon: CSS max-height entfernt, stattdessen JS scrollHeight
- Inline onclick durch data-docs-toggle + Event Listener ersetzt
- Gemeinsame toggleAccordion() Funktion

**Inline-Styles entfernt:**
- Alle ~30 inline style= Attribute durch CSS-Klassen ersetzt
- Neue Utility-Klassen: link-primary, text-source, hero-cta-wrap, explainer-section/text/link
- CO2-Farben: co2-price-low/mid/high/max
- Beispielrechnung: amount-gold, amount-red
- Member-Stats: member-stats-box/number/label/note
- Timeline-Intro: timeline-intro-title/text
- Kontakt: contact-text, contact-links
- Canvas: chart-canvas

**Visual Polish:**
- content-visibility: auto fuer Below-Fold Sections (Performance)
- Enhanced hover-States auf Contact-Cards, AK-Members, Step-Items
- Footer polish: Link-Hover-Animation, E-Mail-Link, Copyright-Link
- Improved responsive Breakpoints

#### Runde 6: Weitere Visual Polish, Responsive Fixes, Standort/Newsletter Sektionen

**Neue CSS-Komponenten (vorbereitet):**
- Standort-Info Sektion: standort-section, standort-grid, standort-card, standort-highlight
- Newsletter/Auf dem Laufenden: newsletter-section, newsletter-channels, newsletter-channel
- Steps Summary: steps-summary (Zusammenfassung der Beitrittsvorteile)

**Dark Mode Erweiterungen:**
- Testimonials Dark-Mode-Styles
- Trust-Badges Dark-Mode-Styles
- Standort-Card Dark-Mode
- Newsletter-Section Dark-Mode
- Steps-Summary Dark-Mode
- Page-Loader Dark-Mode
- Scroll-Progress Dark-Mode

**Responsive Fixes:**
- Testimonial-Grid: 1-spaltig auf <600px
- Trust-Badges: Vertikal-Stack auf <600px
- Newsletter: Kompaktere Padding + vertikale Channels auf <600px
- Standort-Grid: 1-spaltig auf <700px

### 2026-03-03 – Roland Eichmann Rolle aktualisiert
- Aufsichtsrat: Rolle von Roland Eichmann von "1. Buergermeister" zu "Mitglied" geaendert
- Arbeitsgruppe: "Roland Eichmann (1. Buergermeister)" zu "Roland Eichmann (Mitglied)" geaendert

### 2026-03-03 – Aenderungen aus Mails (Jochen Schneider + Simon)
- Schritt 3 "Beitrittserklaerung": Text geaendert — Vollmacht-Satz entfernt, neuer Text "Nach positivem Feedback durch den Vorstand sind Sie Mitglied"
- Schritt 5 "LLV": Text erweitert — LLV kommt vom Vorstand, Hinweis auf Foerderung und Energieberater
- E-Mail korrigiert: alle Vorkommen inkl. Schema.org
- Arbeitsgruppe: "Inn Lindemeyer" → "Inno Lindemeyer"
- Arbeitsgruppe: Matthias Bissinger und Josef Seitz jr. entfernt (jetzt 12 statt 14 Mitglieder)

### 2026-03-03 – Initiale Dokumentation
- Summary-Datei erstellt basierend auf aktuellem Stand der Website

---

*Fuer jede Aenderung bitte einen neuen Eintrag im Changelog mit Datum, Beschreibung und betroffenen Zeilen/Sektionen anlegen.*
