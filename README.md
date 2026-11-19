# CO₂-Vergleich: Gaskraftwerk Schlüchtern und Frankfurter Kreuz

**Ein Hobbyprojekt.** Diese kleine Webanwendung soll den CO₂-Ausstoß des geplanten Gaskraftwerks in Schlüchtern greifbarer machen. 188.000 Tonnen CO₂ pro Jahr sind eine Zahl, unter der sich kaum jemand etwas vorstellen kann. Deshalb stellt die Seite sie einem Ort gegenüber, den viele kennen: dem Frankfurter Kreuz.

Die Seite ist kein amtliches Gutachten und keine wissenschaftliche Studie. Sie ist ein Rechenbeispiel mit offengelegten Annahmen und Quellen. Jede Zahl lässt sich nachvollziehen und in der Seite selbst verändern.

## Öffnen

Die Datei `co2-vergleich-frankfurter-kreuz.html` herunterladen und mit einem Browser öffnen. Es ist keine Installation nötig, und die Seite funktioniert auch ohne Internet. Ohne Internet fällt nur die Schriftart Inter auf eine Systemschrift zurück.

## Was die Seite zeigt

### Einfache Ansicht (Standard)

- Ein Schieberegler für den CO₂-Ausstoß des Kraftwerks von 141.000 bis 400.000 t pro Jahr. Der Ausgangswert ist 188.000 t.
- Das Ergebnis als Faktor, zum Beispiel „4,5× Frankfurter Kreuz im 1,5-km-Kernbereich“, mit einer Reihe von Kreuz-Symbolen.
- Die Bandbreite je nach Annahme, beim Ausgangswert etwa 3,3× bis 6,2×.
- Auf Wunsch blendet eine Fußleiste den Rechenweg und die Quellen ein.

### Detaillierte Ansicht

- Dieselbe Rechnung mit drei Szenarien (niedrige, mittlere und hohe Annahme).
- Eine vereinfachte Vektorgrafik des Frankfurter Kreuzes mit Flugansicht. Sie zeigt, wie groß der 1,5-km-Kernbereich in der Realität ist.
- Eine Tabelle mit allen Annahmen. Jeder Wert ist änderbar, das Ergebnis rechnet sich sofort neu.
- Eine fachliche Einordnung in vier Tabs:
  1. Warum der oft genannte Wert von 45.000 t für das gesamte Kreuz zu niedrig ist
  2. Wie groß die Unsicherheit des Vergleichs ist
  3. Ob der Vergleich fair ist, mit Argumenten dafür und dagegen
  4. Eine Überschlagsrechnung zur Plausibilität der 188.000 t

## Wie gerechnet wird

Verglichen wird nicht das ganze Frankfurter Kreuz, sondern ein klar abgegrenzter **Kernbereich**: je 750 m in jede Richtung ab Kreuzmitte auf A3 und A5, also 1,5 km je Autobahn, plus der Verkehr auf den Verbindungsrampen.

```
CO₂ [t/Jahr] = [ (DTV A3 + DTV A5) × 1,5 km + Abbieger × Rampenlänge ]
               × 365 Tage × Ø g CO₂ pro km ÷ 1.000.000

Ø g CO₂ pro km = (1 − Lkw-Anteil) × EF Pkw + Lkw-Anteil × EF Lkw
```

DTV steht für den durchschnittlichen täglichen Verkehr (Fahrzeuge in 24 Stunden), EF für den Emissionsfaktor.

| | Niedrig | Mittel | Hoch |
|---|---|---|---|
| CO₂ im Kernbereich pro Jahr | ca. 30.000 t | ca. 42.000 t | ca. 57.000 t |
| 188.000 t entsprechen | 6,2× | 4,5× | 3,3× |

**Wichtig:** Die Aussage „4× Frankfurter Kreuz“ gilt nur für den 1,5-km-Kernbereich. Zählt man 5 km je Autobahn, liegt das Kreuz bei rund 131.000 t, und das Verhältnis schrumpft auf etwa 1,4×. Wer den Vergleich verwendet, sollte den Kernbereich deshalb immer mit nennen.

## Datengrundlage

**Gemessen** (amtliche Zählung, Hessen Mobil, Zählwerte 2015):

| Abschnitt | Kfz pro Tag | davon Schwerverkehr |
|---|---|---|
| A3 AS Flughafen – AK Frankfurter Kreuz | 128.877 | 17.891 |
| A3 AK Frankfurter Kreuz – AS Frankfurt-Süd | 141.450 | 18.099 |
| A5 AS Niederrad – AK Frankfurter Kreuz | 156.428 | 13.945 |
| A5 AK Frankfurter Kreuz – AS Zeppelinheim | 143.785 | 14.506 |

**Geschätzt** (in der Seite als Schätzung gekennzeichnet):

- Zahl der Abbieger über die Rampen und deren mittlere Länge
- Emissionsfaktoren als gerundete Spannen: Pkw und leichte Nutzfahrzeuge 150 bis 200 g CO₂/km, Lkw und Busse 700 bis 900 g CO₂/km. Sie orientieren sich an den Größenordnungen des HBEFA. Die HBEFA-Datenbank selbst ist kostenpflichtig, daher werden keine Einzelwerte daraus zitiert.
- Der optionale Zuschlag für die Kraftstoff-Vorkette

**Projektangabe:** 188.000 t CO₂ pro Jahr für das geplante Gaskraftwerk (direkte Emissionen am Standort).

## Quellen

- Hessen Mobil, Straßen- und Verkehrsmanagement: https://mobil.hessen.de
  Verkehrszahlen 2018: https://mobil.hessen.de/sites/mobil.hessen.de/files/2022-02/hmo_verkehrszahlen_2018_a_0.pdf
- Bundesanstalt für Straßenwesen (BASt): https://www.bast.de
- Umweltbundesamt (UBA) und Handbuch für Emissionsfaktoren des Straßenverkehrs (HBEFA): https://www.umweltbundesamt.de
  HBEFA 5.1: https://www.umweltbundesamt.de/themen/hbefa-51-emissionsdatenbank-des-strassenverkehres
  Emissionsdaten Verkehr: https://www.umweltbundesamt.de/themen/verkehr/emissionsdaten

## Grenzen des Vergleichs

- Ein Kraftwerk ist eine einzelne Punktquelle. Das Kreuz ist nur ein kleiner Ausschnitt eines Straßennetzes, auf dem der Verkehr vorher und nachher weiterfährt.
- Der Nutzen beider Seiten (Strom und Wärme gegenüber Mobilität) wird nicht bewertet, nur das CO₂.
- Die 188.000 t hängen von den angenommenen Betriebsstunden des Kraftwerks ab.
- Vorketten (zum Beispiel Methanverluste beim Erdgas oder Emissionen der Raffinerie) sind auf beiden Seiten nicht enthalten.
- Die Kreuz-Grafik ist eine vereinfachte, eigene Zeichnung und keine Karte. Die markierten 1,5 km und der Maßstab sind annähernd maßstäblich, Rampen und Umgebung nur schematisch.

## Technik

- Eine einzige HTML-Datei mit eigenem CSS und JavaScript, ohne Build-Schritt. Einzige Bibliothek ist [marked](https://github.com/markedjs/marked) (MIT-Lizenz) zum Darstellen dieser README. Sie ist direkt in die Datei eingebettet.
- Der (?)-Button lädt diese `README.md` beim Klick neu und stellt sie als Markdown dar. Dazu muss die README im selben Ordner wie die HTML-Datei liegen und die Seite über einen Webserver aufgerufen werden, zum Beispiel GitHub Pages. Wird die HTML-Datei direkt vom Rechner geöffnet, blockiert der Browser das Nachladen. Dann zeigt die Seite eine eingebettete Kopie der README.
- Alle Grafiken (Kraftwerk, Kreuz-Symbole, Kreuz-Ansicht, Silhouette von Schlüchtern) sind als SVG direkt in der Datei enthalten.
- Responsive für Desktop und Smartphone. Die Seite merkt sich die zuletzt gewählte Ansicht im Browser.

## Hinweis

Dieses Projekt entsteht privat und ehrenamtlich. Es soll eine sachliche Diskussion unterstützen. Für Hinweise auf Fehler oder bessere Datenquellen sind wir dankbar.

Stand: November 2026
