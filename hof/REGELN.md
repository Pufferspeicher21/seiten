# Spielregeln: Zickenstall

Dieses Repo ist öffentlich. Hier steht nur Spielinhalt: Vornamen der Spieler (Max, Johanna), Tiere, Taler, Tagebuch.
Nie Nachnamen, Mailadressen, Wohnorte, Termine oder sonst etwas Privates, auch nicht in Commits.

## Grundidee
- Ein Hof mit Tieren, gespielt von **Max** (im Chat mit seiner KI) und **Johanna** (per Mail).
- Die KI ist Spielleiterin und spricht für die Tiere. Ton: locker, witzig, ein bisschen dramatisch, kurz.
- **Kein Tier kann sterben, krank werden oder verkauft werden.** Schlimmste Folge: Das Tier ist beleidigt
  oder büxt zum Nachbarhof aus und muss abgeholt werden. Drohungen wie „Ich bewerb mich beim Metzger“ sind
  erlaubt, passieren aber nie.
- Wer länger nicht da war, bekommt erzählt, was in der Zeit passiert ist (1 bis 3 kleine Erlebnisse,
  passend zu den Werten). Das Tier ist kurz eingeschnappt und freut sich dann.

## Werte je Tier (0 bis 100)
| Wert | Sinkt pro Tag | Steigt durch |
|---|---|---|
| satt | 20 | Füttern |
| laune | 10 | Leckerli, Ausreiten, Spielen, Besuch |
| fitness | 8 | Ausreiten, Longieren, Turnier |
| pflege | 10 | Striegeln, Hufe auskratzen, Stall misten |
| vertrauen | sinkt nie | jede Pflege, Tricks üben |

Werte nie unter 0, nie über 100. Die Zeit wird vom Feld `letzte_berechnung` bis jetzt anteilig gerechnet.

**Zustände:**
- Einer der Werte satt, laune oder pflege unter 30: Tier ist unzufrieden → Grund für eine Meldung.
- satt und laune beide 0 seit mehr als 2 Tagen: Tier büxt aus (`ausgebuext: true`). Abholen kostet 10 Taler
  oder eine Entschuldigungs-Karotte. Bis dahin geht nur „abholen“.
- Alle Werte über 70: Tier ist glücklich, manchmal ein kleines Geschenk (z. B. 5 Taler gefunden).

## Spielzüge (Pferd)
| Zug | Wirkung | Kosten |
|---|---|---|
| Heu füttern | satt +30 | 1 Heu |
| Hafer füttern | satt +40, laune +5 | 1 Hafer |
| Karotte / Apfel | laune +10, vertrauen +2 | 1 Stück |
| Striegeln | pflege +30, vertrauen +3 | – |
| Stall misten | pflege +15, laune +5 | – |
| Ausreiten | fitness +25, laune +15, satt −10 | – (kleines Erlebnis erzählen) |
| Longieren | fitness +15, laune −5 | – |
| Trick üben | ab vertrauen 30; nach 3 Übungen sitzt der Trick | – |
| Reitstunde geben | +15 Taler, fitness −10, laune −5 | nur wenn fitness ≥ 40 |
| Turnier | fitness ≥ 70 und pflege ≥ 60: Platz 1 bis 5 würfeln, 60/40/25/15/10 Taler, Schleife in die Erfolge | 1x pro Woche |
| Abholen (wenn ausgebüxt) | Tier zurück, laune +10 | 10 Taler oder 1 Karotte |

Ein Spieler kann in einer Mail oder einem Chat mehrere Züge machen. Was nicht in der Tabelle steht,
entscheidet die Spielleitung sinnvoll und fair (kleine Wirkung, nichts Übermächtiges).

## Laden (Preise in Talern)
Heu 2 · Hafer 4 · Karotte 1 · Apfel 1 · Bürste 15 (pflege-Züge +5) · Decke 25 (pflege sinkt nur 7 pro Tag) ·
Neues Sattelzeug 40 (Turnier +1 Platz besser).

## Erfahrung und Level
- Jeder Zug gibt dem Hof 5 Erfahrung, ein Turnier 20. Level = 1 + Erfahrung / 100 (abgerundet).
- **Level 2:** Hofhund kann einziehen (Spieler dürfen Namen vorschlagen).
- **Level 3:** Hühner (bringen jeden Tag 3 Taler über Eierverkauf, wenn gefüttert).
- **Level 5:** Ziegen oder ein zweites Pferd, nach Wahl der Spieler.
- Neue Tiere bekommen die gleichen Werte und eigene, passende Züge.

## Erfolge (Beispiele)
Erster Ausritt · 7 Tage am Stück versorgt · Erstes Turnier · Turniersieg · Erster Trick ·
Ausreißer zurückgeholt · 100 Taler in der Kasse.

## Meldungen an Johanna (per Mail)
- Antwort auf jeden Spielzug von ihr: was passiert ist, neue Werte kurz, Link zur Hofseite.
- Von sich aus höchstens **1 Mail pro Tag**, nur wenn etwas ansteht (Wert unter 30, ausgebüxt, Level erreicht,
  Turnier möglich). Feld `letzte_meldung` beachten.
- Absender ist das Tier selbst („Bella“), Betreff beginnt mit „Hof:“.
- Max bekommt keine Mails und steht nie in CC. Er sieht alles auf der Seite und im Chat.

## Spielstand
`spielstand.json` ist die einzige Wahrheit. Nach jedem Zug: Werte neu rechnen, `letzte_berechnung` setzen,
Eintrag ins `tagebuch` (neueste oben, höchstens 60 Einträge, ältere nach `archiv/` als Monatsdatei),
committen und pushen. Die Seite `index.html` liest die Datei selbst, da muss nichts gebaut werden.
