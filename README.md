# ⚓ Roei-examen Training

> Een interactieve, mobielvriendelijke leerwebsite ter voorbereiding op het CWO Roeien I & II theorie-examen bij de Zeeverkenners.

<p align="center">
  <img src="https://img.shields.io/badge/CWO-Roeien_I_%26_II-0B2545?style=for-the-badge" alt="CWO Roeien I & II"/>
  <img src="https://img.shields.io/badge/Modules-21-E0A458?style=for-the-badge" alt="21 modules"/>
  <img src="https://img.shields.io/badge/Single_file-206_KB-8DA9C4?style=for-the-badge" alt="206 KB"/>
</p>

---

## 🎯 Wat is dit?

Een **single-file HTML webapp** (geen framework, geen build-stap, geen dependencies) die een zeeverkenner helpt met het voorbereiden op het CWO roei-examen. Gebouwd met de nadruk op **ADD-vriendelijkheid**: korte chunks, één concept per scherm, instant feedback, en interactieve spelvormen.

Gebaseerd op het *CWO Instructieboek Roeiboot I & II/III* van de Katwijkse Zeeverkenners (Marc van Ruler, 2005) en het officiële theorie-examen Roeien 2022.

### Voor wie?

- Zeeverkenners die zich voorbereiden op het roei-examen
- Leiders die hun waterscouts willen laten oefenen
- Iedereen die de CWO-roeistof wil leren op een toegankelijke manier

---

## ✨ Features

### Leerervaring
- **21 modules** verdeeld over examenstof en CWO-verdieping
- **1 concept per scherm** — swipe door lessons, dan quiz
- **Instant feedback** met uitleg bij elk antwoord
- **Voortgang opgeslagen** in localStorage — ook na sluiten van de browser
- **Examen-modus** met alle 23 examenvragen achter elkaar (ontgrendelt na 3 voltooide modules)

### Interactieve elementen
- 🧩 **Commando-bouwer** — bouw roeicommando's uit losse blokken ("Op riemen" + "Bakboord" + "haalt op" + "Gelijk")
- 🔍 **Vlet-zoekplaatje** — alle 40 vletonderdelen als interactieve naslag + quiz-mode op het officiële examenplaatje
- 🪢 **Touw-eigenschappen-tabel** — filterbaar op gebruik (anker, schoten, landvast) en eigenschap (drijft, kunstvezel)
- 🌤️ **Beaufort-slider** — sleep van 0 tot 12, zie kenmerken én wat het voor de vlet betekent
- 🃏 **Memory-spel** — koppel vletnummers aan kleurcodes
- ⚓ **Examenvragen** met het officiële vletplaatje en oranje highlight-ring per onderdeel

### Visueel
- **Navy-gold-sea kleurenpalet** — rustig, maritiem, niet overweldigend
- **Eigen SVG-illustraties** voor gradenboog (BPR-koersen), lichtcirkels (scheepsverlichting), ankertypes, voorrangsscenario's
- **Officieel examenplaatje** ingebed als base64 — geen externe afbeeldingen nodig
- **Mobile-first** design (max-width 520px), grote tap targets

### Technisch
- **Eén HTML-bestand** — geen build, geen server, geen API
- **~206 KB** totaal inclusief ingebedde afbeeldingen en fonts (Google Fonts: Fraunces + Manrope)
- **Geen cookies, geen tracking, geen ads**
- **localStorage** voor voortgang (key: `roeiexamen_v1`)
- **Deploybaar op Vercel, Netlify, GitHub Pages** of elke statische hosting
- **Architectuur voorbereid** op uitbreiding naar andere CWO-examens (zeilen, motorboot) via het `section`-veld op modules

---

## 📘 Inhoud

### Voor het examen (12 modules)

| Module | Onderwerp | Lessons | Quiz |
|--------|-----------|---------|------|
| ⚓ Knopen | Achtknoop, paalsteek, mastworp, schootsteek, kikker beleggen | 8 | 4 |
| ⛵ Zeiltermen | Bakboord/stuurboord, zeil over bakboord, scheepsrollen | 3 | 3 |
| 🛶 Vletonderdelen | Grendelbout, dolpot, spant + zoekplaatje alle 40 onderdelen | 3 | 3 |
| 📣 Commando's | Halen, strijken, 3 soorten bochten, speciale commando's | 10 | 3 |
| 🪢 Vastleggen | Landvasten, springen, wind-bij-aanleggen-regel | 5 | 3 |
| 🛟 Veiligheid | Omslaan, dode hoek, zuigende/stuwende werking, reddingsvest | 7 | 4 |
| ⚖️ BPR Voorrang | Kruisend/oplopend/tegengesteld, gradenboog, engtes, definities | 9 | 4 |
| 🚥 Betonning | Laterale betonning, kleurcodes, scheidingstonnen | 4 | 2 |
| 🚫 Borden | Verbods-, aanwijzings-, aanbevelings- en gebodstekens | 7 | 5 |
| 🌉 Bruggen & Sluizen | Brugseinen (in/buiten bedrijf), sluistekens | 3 | 2 |
| 🔺 Tekens van schepen | Zwarte bol, zwarte kegel, dagtekens, cilinder, blauwe kegel | 3 | 3 |
| 🎨 Kleurcodes | 7 vletten koppelen aan kleuren (memory-spel) | 2 | 4 |

### CWO Verdieping (9 modules)

| Module | Onderwerp | Speels element |
|--------|-----------|----------------|
| 🎯 Manoeuvres | Achtje, afvaren, aanleggen, man overboord, ankeren | — |
| 🚣 Vaartechnieken | Wrikken, jagen, slepen | — |
| 🧩 Commando-bouwer | 8 opdrachten: bouw het juiste commando | **Interactief spel** |
| 💡 Scheepsverlichting | Boordlichten, toplicht, heklicht per bootgrootte | Lichtcirkel-SVG |
| 📢 Geluidsseinen | Korte/lange stoten, ezelsbruggetjes | — |
| 🌤️ Het weer | Beaufort 0–12, ruimende/krimpende wind, onweer | **Beaufort-slider** |
| 🛠️ Onderhoud | Dagelijks + winter (6 stappen), verftips, 4 ankertypes | Anker-SVGs |
| 🪢 Touwen & ankers | 9 touwsoorten, natuur- vs kunstvezel, 4 ankertypes | **Filter-tabel** |
| 🎌 Etiquette | Gedragsregels, vlagvoering, omslaan | — |

---

## 🚀 Deployment

### Optie 1: Vercel (aanbevolen)

Drop `roeien.html` in je Vercel-project en deploy. Klaar.

```
project/
├── public/
│   └── roeien.html    ← of als index.html
└── vercel.json         ← optioneel
```

### Optie 2: GitHub Pages

1. Maak een repo aan
2. Zet `roeien.html` als `index.html` in de root
3. Ga naar Settings → Pages → Source: main branch
4. Klaar — live op `https://username.github.io/repo-naam/`

### Optie 3: Gewoon lokaal openen

Dubbelklik op `roeien.html` in je browser. Alles werkt offline behalve de Google Fonts (die vallen dan terug op systeemfonts).

---

## 🏗️ Architectuur

```
roeien.html
├── <style>           CSS (variabelen, mobile-first layout, component-stijlen)
├── <body>            Minimale HTML-shell (header + main container)
└── <script>
    ├── SVG helpers         Knoop-SVGs, voorrangs-SVGs, vlet-plaatje, lichtcirkel, gradenboog, ankers
    ├── Game helpers        Commando-bouwer, vlet-zoekplaatje, touw-tabel, Beaufort-slider, memory
    ├── MODULES[]           21 module-objecten met lessons[], quiz[], section, custom hooks
    ├── EXAMEN{}            23 officiële examenvragen (Roeien I, Roeien II, BPR)
    ├── State management    localStorage read/write, progress tracking
    ├── Router/renderer     Home → Module → Lesson → Quiz → Result flow
    └── Examen-modus        Aparte flow met per-sectie scoring
```

### Module-structuur

```javascript
{
  id: 'knopen',
  section: 'exam',           // 'exam' | 'verdieping'
  icon: '⚓',
  title: 'Knopen',
  desc: 'Korte beschrijving',
  custom: 'memory',          // optioneel: triggert een game-init
  lessons: [
    { title: 'Achtknoop', body: `<p>HTML content</p>`, custom: 'memory' }
  ],
  quiz: [
    { q: 'Vraag?', opts: ['A','B','C','D'], correct: 2, why: 'Uitleg' }
  ]
}
```

Het `section`-veld maakt het mogelijk om later andere CWO-examens toe te voegen (zeilen, motorboot, kielboot) als aparte secties, zonder de bestaande structuur te breken.

---

## 🎨 Design tokens

| Token | Waarde | Gebruik |
|-------|--------|---------|
| `--navy` | `#0B2545` | Primaire tekst, headers |
| `--gold` | `#E0A458` | Accenten, highlights, progress |
| `--sea` | `#8DA9C4` | Secundaire elementen |
| `--cream` | `#FBF8F3` | Achtergrond |
| `--red` | `#C44536` | Fouten, bakboord |
| `--green` | `#2D6A4F` | Correct, stuurboord |

Fonts: [Fraunces](https://fonts.google.com/specimen/Fraunces) (serif, headers) + [Manrope](https://fonts.google.com/specimen/Manrope) (sans, body).

---

## 📱 Screenshots

De website is mobile-first ontworpen (max-width 520px) en werkt op elke telefoon, tablet of desktop.

**Homepage** met twee secties (examenstof + verdieping), voortgangsbalk, en examen-CTA.

**Lesson-weergave** met navigatie-dots bovenaan, één concept per scherm, en visuele illustraties.

**Quiz** met 4 opties, instant feedback en uitleg.

**Commando-bouwer** waar je zelf het juiste commando samenstelt uit losse blokken.

**Beaufort-slider** waar je van 0 tot 12 schuift en per windkracht de kenmerken + vlet-advies ziet.

---

## 🔧 Aanpassen

### Modules toevoegen

Voeg een nieuw object toe aan de `MODULES[]` array:

```javascript
{
  id: 'nieuw-onderwerp',
  section: 'verdieping',
  icon: '🆕',
  title: 'Nieuw onderwerp',
  desc: 'Korte beschrijving',
  lessons: [
    { title: 'Les 1', body: `<p>Inhoud hier</p>` }
  ],
  quiz: [
    { q: 'Vraag?', opts: ['A','B','C','D'], correct: 0, why: 'Uitleg' }
  ]
}
```

### Examenvragen aanpassen

De examenvragen staan in het `EXAMEN` object, opgedeeld in `roeien1`, `roeien2`, en `bpr`. Elk object volgt hetzelfde `{q, opts, correct, why}` patroon als de module-quizzes, met optioneel een `img` veld voor SVG-illustraties.

### Custom games toevoegen

1. Maak een `initMijnGame()` functie aan in de helpers-sectie
2. Voeg `custom: 'mijngame'` toe aan de lesson
3. Hook de init op in de `renderLesson()` functie:
   ```javascript
   else if(lesson.custom === 'mijngame'){ initMijnGame(); }
   ```
4. Zorg dat de lesson body een `<div id="mijnGame"></div>` bevat als container

### Voortgang resetten

Er is een reset-knop in de UI (tandwiel-icoon rechtsboven). Programmatisch:

```javascript
localStorage.removeItem('roeiexamen_v1');
location.reload();
```

---

## 📄 Bronnen

- **CWO Instructieboek Roeiboot I & II/III** — Marc van Ruler, St. de Katwijkse Zeeverkenners, 1e druk december 2005
- **Theorie-examen Roeien 2022** — met antwoordblad
- **Presentatie Roeien 12-2026** — 45 slides cursusmateriaal

---

## 📝 Licentie

Dit project is gemaakt voor educatief gebruik binnen de Zeeverkenners / Scouting Nederland. De inhoud is gebaseerd op het CWO instructieboek van de Katwijkse Zeeverkenners (© Katwijkse Zeeverkenners).

---

## 🙏 Credits

Gebouwd door Leander met hulp van Claude (Anthropic). Alle inhoud is afkomstig uit het CWO instructieboek en het officiële theorie-examen.

Het officiële vletplaatje in de quiz is afkomstig uit het examen en wordt met toestemming gebruikt.
