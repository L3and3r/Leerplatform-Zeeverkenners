# Leerplatform ZV Canisius — Handleiding voor instructeurs

Dit leerplatform bestaat uit drie bestanden die **naast elkaar** moeten staan:

| Bestand | Wat staat erin |
|---|---|
| `leerplatform.html` | De app zelf — **niet aanraken** |
| `vragen.json` | Alle quiz- en examenvragen — **hier bewerk je** |
| `modules.json` | Alle lesinhoud (tekst, uitleg) — **hier bewerk je** |

Open de bestanden met een gewone teksteditor (Kladblok, Notepad++, VS Code).
Sla altijd op als **UTF-8** (standaard in alle moderne editors).

---

## Een vraag corrigeren

Open `vragen.json` en zoek de vraag op (Ctrl+F op een stukje vraagtekst).

Elke vraag ziet er zo uit:

```json
{
  "vraag": "Welke kleur heeft een bakboordlicht?",
  "opties": ["Rood", "Groen", "Wit", "Geel"],
  "correct": 0,
  "uitleg": "Bakboord is altijd rood."
}
```

Wat je mag aanpassen:

- **`vraag`** — de vraagtekst
- **`opties`** — de vier antwoordmogelijkheden (altijd vier stuks)
- **`correct`** — het nummer van het juiste antwoord: `0` = eerste optie, `1` = tweede, `2` = derde, `3` = vierde
- **`uitleg`** — de toelichting die na het antwoord verschijnt

> Velden `afbeelding` of `diagram` bevatten tekencodes (`{{svg:...}}`). Laat die **ongemoeid**.

---

## Een vraag toevoegen

Zoek in `vragen.json` de juiste plek op, bijvoorbeeld onder `roeien › modules › knopen › quiz` of `zeilen › lichtmatroos › examen`.

Voeg een nieuw vraagobject toe **binnen de rechte haken** `[...]`, gescheiden door een komma:

```json
{
  "vraag": "Jouw nieuwe vraag?",
  "opties": ["Optie A", "Optie B", "Optie C", "Optie D"],
  "correct": 2,
  "uitleg": "Uitleg waarom optie C juist is."
}
```

---

## Een vraag verwijderen

Verwijder het hele vraagblok `{ ... }` inclusief de komma die ervoor of erna staat.
Zorg dat de lijst nog steeds geldig JSON is (geen komma na het laatste item).

---

## Lesinhoud aanpassen

Open `modules.json`. Lesinhoud staat onder `lessen › inhoud` per module.
De tekst is HTML — je mag de zichtbare tekst aanpassen.

**Niet aanpassen:** alles binnen `{{svg:...}}` (dat zijn tekeningen) en HTML-tagnamen.

---

## Een nieuw zeilvaartniveau toevoegen (bv. Lichtblauw)

### Stap 1 — Voeg modules toe in `modules.json`

Zoek de sleutel `"zeilen"` en voeg onderaan een nieuw blok toe:

```json
"lichtblauw": {
  "naam": "Zeilen Lichtblauw",
  "icoon": "🔵",
  "kleur": "#1E90FF",
  "modules": [
    {
      "id": "lb_knopen",
      "sectie": "exam",
      "icoon": "⚓",
      "titel": "Knopen Lichtblauw",
      "beschrijving": "Korte omschrijving",
      "lessen": [
        { "titel": "Paalsteek", "inhoud": "<p>Uitleg hier.</p>" }
      ]
    }
  ]
}
```

### Stap 2 — Voeg vragen toe in `vragen.json`

Zoek de sleutel `"zeilen"` en voeg onderaan toe:

```json
"lichtblauw": {
  "modules": {
    "lb_knopen": {
      "quiz": [
        {
          "vraag": "Eerste oefenvraag?",
          "opties": ["A", "B", "C", "D"],
          "correct": 0,
          "uitleg": "Uitleg."
        }
      ]
    }
  },
  "examen": [
    {
      "vraag": "Eerste examenvraag?",
      "opties": ["A", "B", "C", "D"],
      "correct": 1,
      "uitleg": "Uitleg."
    }
  ]
}
```

**De sleutelnaam (`"lichtblauw"`) moet in beide bestanden identiek zijn.**
De app herkent het nieuwe niveau automatisch — geen codewijzigingen nodig.

---

## Controleren of JSON geldig is

Kopieer de inhoud van het bestand naar **jsonlint.com** en klik op "Validate".
Veelgemaakte fouten: komma vergeten, komma te veel, aanhalingsteken mist.

---

## Iets kapot? Origineel terugzetten

Een reservekopie van de originele HTML staat in `leerplatform.html.bak`.
De JSON-bestanden hebben geen automatische backup — maak zelf een kopie voor je begint.
