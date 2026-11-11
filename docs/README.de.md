<p align="center">
  <a href="../README.md">English</a> ·
  <a href="README.fr.md">Français</a> ·
  <strong>Deutsch</strong> ·
  <a href="README.es.md">Español</a> ·
  <a href="README.it.md">Italiano</a> ·
  <a href="README.pt.md">Português</a>
</p>

<p align="center">
  <img src="images/hero.svg" alt="Thierry Skill: Art Direction für das Web, nach Maß" width="100%">
</p>

# Thierry Skill

**Ein Art Director für Claude.** Mit diesem Skill gestaltet Claude Websites so, wie ein gutes Studio arbeitet: Er findet eine Idee im Handwerk des Kunden, leitet daraus ein vollständiges visuelles System ab, baut die Seite, sieht sich das gerenderte Ergebnis an und bewertet es, bevor die Arbeit als fertig gilt.

[![Lizenz: MIT](https://img.shields.io/badge/Lizenz-MIT-14161a.svg)](../LICENSE)
![Für Claude Code](https://img.shields.io/badge/Claude_Code-Skill-e5412d.svg)
![Sprache des Skills: Französisch](https://img.shields.io/badge/Sprache_des_Skills-Französisch-5c6370.svg)

```bash
npx skills@latest add Jacckisback/thierry-skills
```

## Das Problem

KI-Agenten schreiben korrekten Interface-Code. Was ihnen fehlt, ist eine Haltung. Wer „eine schöne, moderne Website“ verlangt, bekommt den Durchschnitt aller Websites: dieselbe Schrift, denselben violetten Verlauf, dieselben drei Karten mit Icons. Nichts ist falsch, und nichts bleibt im Gedächtnis.

Bestehende Design-Skills polieren vor allem die Oberfläche: Kurven, Dauern, Mikrointeraktionen. Diese Arbeit zählt, kommt aber zuletzt. Eine Seite mit perfekten Animationen und ohne Idee bleibt eine Vorlage.

## Was dieser Skill ändert

Er lässt Claude drei Fragen beantworten, in dieser Reihenfolge, bevor ein einziger Effekt hinzukommt:

1. **Was ist die Idee?** Ein Satz, der etwas Genaues über diesen Kunden sagt, das die Seite eines Mitbewerbers nicht sagen könnte.
2. **Was ist das System?** Schrift, Farbe, Raum, Form, Bild, Stimme und Bewegung, alle aus dieser Idee abgeleitet.
3. **Stimmt es auf dem Bildschirm?** Screenshots in drei Breiten, gemessen und bewertet.

Zwei Briefings aus je einem Satz, zwei Ergebnisse ohne Gemeinsamkeit:

<table>
  <tr>
    <td width="50%"><img src="images/demo-luthier.png" alt="Startseite eines Gitarrenbauers, gesetzt wie das Auftragsbuch der Werkstatt"></td>
    <td width="50%"><img src="images/demo-pour-contre.png" alt="Erster Bildschirm der Seite einer Arbeitsrechtsanwältin: FÜR die Arbeitnehmer, GEGEN ihren Arbeitgeber"></td>
  </tr>
  <tr>
    <td><em>„Eine Website für einen Flamencogitarrenbauer in Madrid, drei Gitarren im Monat, auf Bestellung.“</em><br>Idee: das Auftragsbuch der Werkstatt. Drei Zeilen im Monat, eine davon kann Ihren Namen tragen.</td>
    <td><em>„Eine Website für eine Arbeitsrechtsanwältin in Lyon, die ausschließlich Arbeitnehmer vertritt.“</em><br>Idee: ein Schriftsatz. „Für: die Arbeitnehmer. Gegen: ihren Arbeitgeber.“</td>
  </tr>
</table>

Beide Seiten hat der Skill während der Tests aus fiktiven Briefings erzeugt. Nach seinem eigenen Raster erreichten sie 81 und 82 von 100 Punkten. Das liegt unter seiner Schwelle von 85, vor allem weil ein Briefing aus einem Satz keine echten Fotos, Preise oder Belege enthält und der Skill solche Stellen als „noch zu liefern“ kennzeichnet, statt etwas zu erfinden.

## Art Direction, erklärt

Eine Website ist schön, wenn drei Dinge zugleich zutreffen:

- **Eine Idee.** Sie sagt etwas Bestimmtes über ihren Gegenstand.
- **Ein System.** Jede visuelle Entscheidung folgt aus dieser Idee, und die Entscheidungen antworten aufeinander.
- **Eine Ausführung.** Jedes unsichtbare Detail stimmt: Ausrichtung, Zustände, Rhythmus, Tempo, Barrierefreiheit.

Die meisten Websites verfehlen den ersten Punkt und gleichen das mit Effekten aus. Ein Effekt ist nie eine Idee.

Der Skill sucht die Idee in dem, woraus das Handwerk besteht: Gegenstände, Dokumente, Handgriffe, Orte, Materialien, Wörter und Maße. Ein Weinhändler hat Etiketten und Verkostungsnotizen. Eine Architektin hat Pläne und Schnitte. Ein Anwalt hat Schriftsätze. Diese Formen gehören dem Kunden bereits, deshalb lässt sich eine daraus gebaute Seite mit keiner anderen verwechseln.

Der zentrale Test ist der **Logotausch**: Man ersetzt das Logo durch das eines direkten Mitbewerbers. Funktioniert die Seite weiterhin, gibt es keine Idee, und die Arbeit beginnt von vorn.

<p align="center">
  <img src="images/process.svg" alt="Die sieben Schritte des Skills" width="100%">
</p>

*Die sieben Schritte: verstehen, die Idee finden, die Persönlichkeit einstellen, das System bauen, komponieren, ausführen, ansehen und bewerten.*

### Persönlichkeit in Zahlen

„Warm“, „seriös“ oder „mutig“ sagen einem Stylesheet nichts. Der Skill setzt sieben Regler von 0 bis 10 (Temperatur, Dichte, Energie, Ornament, Epoche, Tonlage, Kontrast) und übersetzt jeden in konkrete Parameter: Radien, Schriftstärken, Laufweite, Dauern, Abstände, Sättigung. Zwei Unternehmen derselben Branche erhalten unterschiedliche Einstellungen. Daraus entsteht Maßarbeit.

<p align="center">
  <img src="images/sliders.svg" alt="Sieben Persönlichkeitsregler für zwei Richtungen desselben Handwerks" width="100%">
</p>

## In Zahlen

| | |
| --- | --- |
| **7** | Schritte vom Briefing bis zur Prüfung |
| **9** | Gesetze, die der Skill ohne ausdrückliche Bitte nie bricht |
| **7** | Persönlichkeitsregler, jeder auf genaue Werte abgebildet |
| **21** | Branchen, mit den Erwartungen der Besucher, den zu meidenden Klischees und zwei gegensätzlichen Richtungen |
| **10** | Architekturen für den ersten Bildschirm zur Auswahl |
| **11** | Referenzdateien, rund 30.000 Wörter, nur bei Bedarf geladen |
| **6** | Sprachen mit typografischen Regeln: Französisch, Spanisch, Deutsch, Englisch, Italienisch, Portugiesisch |
| **35** | statische Prüfungen am Code (`audit.mjs`) |
| **22** | Prüfungen an der gerenderten Seite (`regard.mjs`) |
| **100** | Punkte im Bewertungsraster, verteilt auf 9 gewichtete Achsen |

## Er prüft seine eigene Arbeit

Ein Entwurf, der nur durch Lesen des Codes beurteilt wurde, ist nicht beurteilt. Der letzte Schritt ist Pflicht: aufnehmen, ansehen, bewerten, korrigieren.

`regard.mjs` öffnet die Seite in einem echten Browser in drei Breiten. Es speichert den ersten Bildschirm, die ganze Seite, lesbare Ausschnitte, eine Graustufenversion und eine unscharfe Version und misst dann, was dem Auge entgeht.

<table>
  <tr>
    <td width="33%"><img src="images/regard-ecran.png" alt="Aufnahme des ersten Bildschirms"></td>
    <td width="33%"><img src="images/regard-gris.png" alt="Aufnahme in Graustufen"></td>
    <td width="33%"><img src="images/regard-flou.png" alt="Unscharfe Aufnahme"></td>
  </tr>
  <tr>
    <td><strong>Erster Bildschirm.</strong> Der Fünf-Sekunden-Test: Was behält ein Fremder?</td>
    <td><strong>Graustufen.</strong> Hält die Hierarchie ohne Farbe?</td>
    <td><strong>Unscharf.</strong> Der Blinzeltest: eine dominante Fläche, dann eine zweite, dann der Rest.</td>
  </tr>
</table>

Bei jedem Durchlauf gemessen: Textkontrast nach den WCAG-Schwellen, horizontaler Überlauf, Touch-Ziele unter 24 und 44 px, Zeilenlänge, tatsächlich dargestellte Schriftfamilien und -größen, nicht geladene Schriften, Bilder ohne Maße oder Alternativtext, Überschriftenstruktur, Felder ohne Beschriftung, Layoutverschiebungen und alles, was sich noch bewegt, obwohl der Besucher reduzierte Bewegung verlangt hat.

`audit.mjs` liest den Quellcode und meldet Vorlagengewohnheiten und Ausführungsfehler: `transition: all`, Eingänge aus `scale(0)`, entfernte Fokusringe, violette Verläufe, Blindtext, vage Button-Beschriftungen, falsche französische Interpunktion.

Danach wird die Seite bewertet. Unter 85 Punkten werden die drei schwersten Schwächen behoben und die Seite erneut aufgenommen.

<p align="center">
  <img src="images/score.svg" alt="Das Bewertungsraster mit 100 Punkten" width="100%">
</p>

*Das Raster: Idee und Persönlichkeit 20, Typografie 15, Komposition 15, Farbe und Form 10, Inhalt und Stimme 10, Feinschliff 10, Barrierefreiheit und Performance 10, Bild 5, Bewegung 5.*

## Was Sie verlangen können

| Sie sagen | Der Skill liefert |
| --- | --- |
| „Erstelle eine Website für …“ | ein Art-Direction-Blatt, den Code, dann eine Prüfung anhand von Screenshots |
| „Überarbeite diese Website“ | eine Diagnose, was bleibt, eine neue Richtung, ein Vorher und Nachher |
| „Was hältst du davon?“ | eine Note von 100 und geordnete Korrekturen, ohne etwas zu ändern |
| „Feile daran“ | Feinschliff, der das Konzept unberührt lässt |
| „Das wirkt beliebig“, „das sieht nach KI aus“ | die Liste der gefundenen Gewohnheiten und was jede ersetzt |
| „Gib mir Varianten“ | drei Richtungen, die sich im Konzept unterscheiden, nicht in der Farbe |
| „Lovable-Prompt“ | einen fertigen Prompt für Lovable oder einen anderen Website-Generator |

## Installation

```bash
npx skills@latest add Jacckisback/thierry-skills
```

Oder von Hand: Kopieren Sie `skills/thierry-skill` in den Ordner `.claude/skills/` Ihres Projekts oder nach `~/.claude/skills/`, um den Skill überall zu haben. In den Claude-Apps packen Sie den Ordner `skills/thierry-skill` als ZIP und laden ihn in den Skill-Einstellungen hoch.

Beide Skripte benötigen Node 18 oder neuer. `regard.mjs` braucht zusätzlich Playwright mit Chromium:

```bash
npm i -D playwright
```

```bash
npx playwright install chromium
```

## Verwendung

Ein Satz genügt:

> Nutze thierry-skill: Erstelle die Startseite für eine Naturweinhandlung in Madrid.

Der Skill ist auf Französisch geschrieben und antwortet in der Sprache, in der Sie schreiben. Er baut Websites in jeder Sprache.

Die Skripte lassen sich jederzeit selbst starten:

```bash
node skills/thierry-skill/scripts/regard.mjs http://localhost:3000 --out pruefung
```

```bash
node skills/thierry-skill/scripts/audit.mjs ./src
```

## Inhalt

```
skills/thierry-skill/
├── SKILL.md                         Prozess, Gesetze, Ausgabeformate
├── references/
│   ├── 01-direction-artistique.md   Konzept, Signatur, Umrechnung der Regler
│   ├── 02-univers-par-secteur.md    21 Branchen: Erwartungen, Klischees, je zwei Richtungen
│   ├── 03-typographie.md            Auswahl, Paarung, Skala, Feineinstellung, Laden
│   ├── 04-couleur.md                OKLCH-Paletten, Kontrast, Dunkelmodus
│   ├── 05-composition.md            Raum, Raster, erster Bildschirm, Bild, Mobil
│   ├── 06-mouvement.md              wann animieren, Kurven, Dauern, Choreografie
│   ├── 07-finitions.md              Zustände, Formulare, Barrierefreiheit, Performance, SEO
│   ├── 08-anti-generique.md         die „KI-Gewohnheiten“ und ihr Ersatz
│   ├── 09-ecriture.md               Überschriften, Buttons, Typografie in sechs Sprachen
│   ├── 10-revue.md                  das 100-Punkte-Raster und das Prüfformat
│   └── 11-brief-lovable.md          Prompt-Vorlage mit ausgefülltem Beispiel
├── assets/tokens.css                neutrale CSS-Variablen zum Anpassen
└── scripts/
    ├── regard.mjs                   Screenshots und Messungen
    └── audit.mjs                    statische Codeprüfung
```

## Das Ziel

Websites, die nur ihrem Inhaber gehören können. Ein Besucher soll die Seite am nächsten Tag aus dem Gedächtnis beschreiben können, und der Kunde soll darin sein eigenes Handwerk wiedererkennen. Der Skill versteht Schönheit als Ergebnis von Genauigkeit: eine wahre Idee, ein strenges System und ein Beweis auf dem Bildschirm.

## Grenzen

- Er ersetzt die Inhalte des Kunden nicht. Ohne echte Fotos, Preise und Belege kennzeichnet er die Stellen, und die Note bleibt gedeckelt.
- Die Richtungen je Branche sind Ausgangspunkte. Unverändert übernommen, ergäben sie für jedes Unternehmen einer Branche dieselbe Seite.
- Die Skripte liefern Hinweise, die mit dem Auge zu prüfen sind. Sie testen weder Tastaturbedienung noch Formularzustände noch Screenreader.
- Die Ergebnisse hängen vom Modell ab, das den Skill ausführt, und wurden bisher nur an zwei Briefings getestet.

## Herkunft

Dieser Skill entstand aus der genauen Lektüre der [Skills von Emil Kowalski](https://github.com/emilkowalski/skills), die Animation und Interface-Details sehr präzise behandeln. Er erweitert das Feld auf vollständige Art Direction und ergänzt die Prüfung des gerenderten Ergebnisses. Text und Code sind eigenständig.

## Lizenz

[MIT](../LICENSE)
