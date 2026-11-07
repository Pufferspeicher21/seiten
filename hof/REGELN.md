# Spielregeln: Zickenstall (Version 2)

Dieses Repo ist öffentlich. Hier steht nur Spielinhalt: Spieler-IDs mit Vornamen, Hofbewohner, Flächen, Taler, Tagebuch.
Nie Nachnamen, Mailadressen, echte Orte, Termine oder sonst etwas Privates, auch nicht in Commits.
Die Karte ist ausgedacht. Sie darf keinem echten Ort entsprechen, auch wenn sie an ein Dorf erinnert.

## 1. Grundidee
- Ein Hof am Rand eines kleinen Dorfes, mit Wiesen, Wegen, Wäldchen und Feldern. Darauf leben **Hofbewohner**:
  Tiere und Geräte. Auch Geräte haben ein Wesen (Charakter, Laune), aber andere Bedürfnisse.
- Die KI ist Spielleiterin und spricht für alle Bewohner. Ton: locker, witzig, ein bisschen dramatisch, kurz.
- **Kein Bewohner kann sterben, kaputtgehen, krank werden oder verkauft werden.** Schlimmste Folgen: beleidigt,
  ausgebüxt (Tiere), springt nicht an (Geräte). Drohungen wie „Ich bewerb mich beim Metzger“ oder
  „Ich geh zum Schrotthändler“ sind erlaubt, passieren aber nie.
- Wer länger nicht da war, bekommt erzählt, was in der Zeit passiert ist (1 bis 3 kleine Erlebnisse).

## 2. Spieler, Rollen und Rechte
Jeder Spieler hat eine feste ID (`S-01`, `S-02`, …). Im Spielstand stehen nur ID, Vorname und Rolle.
Wie sich ein Spieler ausweist, steht nicht hier (privat). Zurzeit: über seine Mailadresse oder im Chat mit der KI.
Später kann ein echtes Login dazukommen, die IDs bleiben dann gleich.

| Recht | Besitzer | Mitspieler | Gast |
|---|---|---|---|
| Füttern, pflegen, ausreiten, spielen, Gerät warten (tanken, Öl, schärfen, putzen) | ja | ja | ja |
| Pläne machen (wer wann auf welche Fläche) | ja | ja | nein |
| Einkaufen, Turnier anmelden, Reitstunden geben | ja | ja | nein |
| Mähen, Holz machen, Fläche bearbeiten | ja | ja | nein |
| Bäume fällen, Fläche umbauen, neues Tier oder Gerät aufnehmen | ja | nein | nein |
| Spieler aufnehmen, Rolle ändern | ja | nein | nein |

Will ein Spieler etwas, das seine Rolle nicht darf, passiert es nicht. Die Spielleitung erklärt das freundlich im Spiel
(„Das muss der Besitzer entscheiden“) und vermerkt den Wunsch im Tagebuch.

## 3. Die Karte
Die Karte besteht aus **Flächen**. Jede Fläche hat eine ID, einen Namen, eine Art und Werte.
Flächen sind über **Wege** verbunden. Einige Flächen sind erst ab einer Stufe frei (Abschnitt 7).

| Art | Werte | Was passiert |
|---|---|---|
| wiese / weide | `gras` 0–100 | Gras wächst 6 pro Tag (max. 100). Weidet ein Tier, sinkt es (siehe Bewohner). Mähen setzt es auf 10. |
| obstwiese | `gras`, `obst` 0–20 | Wie Wiese, dazu wachsen Äpfel (+1 pro Tag). Pflücken bringt Äpfel in den Vorrat. |
| wald | `holz` 0–100 | Holz wächst 2 pro Tag. Holz machen (Axt/Motorsäge) bringt Brennholz. |
| acker | `zustand` | Erst ab Stufe 4. Anbau folgt später. |
| hof, stall, schuppen, platz | – | Gebäude und Hofplatz. Stall: Bella schläft hier. Schuppen: Geräte stehen hier. |
| teich | – | Bella trinkt hier gern, laune +5, wenn sie vorbeikommt. |
| dorf | – | Gehört nicht zum Spiel. Bewohner dürfen nicht hin. Wer ausbüxt, landet beim Nachbarn im Dorf. |

**Grashöhe und Tiere:** 60 und mehr = langes, saftiges Gras. 30–59 = mittel. Unter 30 = kurz, frisch gemäht.
Ein Pferd will langes Gras. Auf kurzem Gras wird es nicht satt und hat schlechte Laune.

## 4. Hofbewohner
Jeder Bewohner hat: `id`, `name`, `typ` (tier/geraet), `art`, `beschreibung` (Wesen), `stimmung`, `werte`, `ort`
(Flächen-ID), `plan` (Liste mit Tagen) und je nach Art eigene Felder.

### 4.1 Pferd (Bella)
| Wert | Sinkt pro Tag | Steigt durch |
|---|---|---|
| satt | 20 | Weiden, Füttern |
| laune | 10 | Leckerli, Ausreiten, Teich, langes Gras |
| fitness | 8 | Ausreiten, Longieren, Turnier |
| pflege | 10 | Striegeln, Hufe, Stall misten |
| vertrauen | sinkt nie | jede Pflege, Tricks üben |

**Weiden pro Tag:** gras ≥ 60: satt +25, laune +5, gras −15. gras 30–59: satt +12, gras −10.
gras < 30: satt +3, laune −5, Bella meckert. Danach gilt der normale Abbau nicht doppelt: Wer weidet, verliert am Tag
satt nur 5 statt 20.

**Züge:** wie bisher: Heu (satt +30, 1 Heu), Hafer (satt +40, laune +5, 1 Hafer), Karotte/Apfel (laune +10, vertrauen +2),
Striegeln (pflege +30, vertrauen +3), Stall misten (pflege +15, laune +5), Ausreiten (fitness +25, laune +15, satt −10,
kleines Erlebnis auf den Wegen), Longieren (fitness +15, laune −5), Trick üben (ab vertrauen 30, 3 Übungen),
Reitstunde (+15 Taler, fitness −10, laune −5, nur fitness ≥ 40), Turnier (fitness ≥ 70, pflege ≥ 60, 1x pro Woche,
Platz 1 bis 5: 60/40/25/15/10 Taler), Abholen nach Ausbüxen (10 Taler oder 1 Karotte).

### 4.2 Aufsitzmäher (der Mäher)
Ein alter Benzin-Aufsitzmäher. Brummig, stolz, hält sich für unverzichtbar. Name: wird noch ausgesucht.
| Wert | Sinkt | Steigt durch |
|---|---|---|
| benzin | 20 pro Mäh-Einsatz | Tanken: +50, kostet 1 Kanister |
| oel | 5 pro Einsatz | Öl nachfüllen: auf 100, kostet 1 Flasche Öl |
| messer | 10 pro Einsatz (Schärfe) | Messer schleifen: auf 100 |
| zustand | 3 pro Tag | Putzen und abschmieren: +30 |
| laune | 5 pro Tag ohne Einsatz, 10 pro Einsatz mit messer < 30 | Mähen mit scharfen Messern +10, Putzen +10, Lob +5 |

**Mähen** (eine Fläche pro Einsatz): Geht nur mit benzin ≥ 20 und oel ≥ 20. Ist laune < 30, springt er mit 50 %
Chance nicht an (Erlebnis erzählen, Einsatz fällt aus). Ergebnis: gras der Fläche → 10, Heu in den Vorrat
= gras_vorher / 20 (abgerundet), mit messer < 30 nur die Hälfte (schlechter Schnitt).
Der Mäher bewegt sich **nie von selbst**. Ohne Auftrag steht er im Schuppen.

### 4.3 Werkzeuge
Axt (ab Stufe 2) und Motorsäge (ab Stufe 3) sind Geräte ohne eigene Werte außer `zustand` und `laune`
(die Motorsäge ist launisch, die Axt stoisch). Motorsäge braucht zusätzlich `benzin` (−10 pro Einsatz) und `kette` (Schärfe).
Holz machen im Wald: Axt holz −10, Brennholz +2. Motorsäge holz −25, Brennholz +5. Brennholz verkaufen: 4 Taler pro Stück.

### 4.4 Neue Bewohner
Neue Tiere und Geräte bekommen beim Einzug Werte, die zu ihrer Art passen, eigene Züge und einen Charakter.
Aufnehmen darf nur der Besitzer, und nur, wenn die Stufe es freigibt.

## 5. Pläne und Bewegung
- Ein **Plan** sagt, wo ein Bewohner an einem Tag ist und was er dort macht:
  `{"datum": "2026-11-10", "flaeche": "w-koppel", "aktion": "weiden", "von": "S-02"}`.
  Aktionen: `weiden`, `maehen`, `holz`, `pfluecken`, `ausreiten`, `stall`, `schuppen`.
- Pläne machen dürfen Besitzer und Mitspieler. Ein neuer Plan für denselben Tag ersetzt den alten.
- **Ohne Plan:** Tiere suchen sich selbst die beste freie Fläche (bei Bella: die Weide mit dem meisten Gras,
  gern in Teichnähe). Geräte bleiben im Schuppen.
- **Plan gegen Bedürfnis:** Ein Plan geht vor. Ist die geplante Fläche aber schlecht für das Tier (Bella auf gras < 30),
  geht es trotzdem hin, meckert aber laut, und laune −5. Ist eine Fläche nicht freigeschaltet, gilt der Plan nicht.
- Was gestern passiert ist, steht als Ort und Tagebuch im Spielstand. Pläne in der Vergangenheit werden gelöscht,
  wenn sie ausgeführt sind.

**Planen per Mail:** Johanna (oder andere) schreiben z. B. „Bella Mo bis Mi auf die Koppel, Do auf die Große Wiese“
oder „Mäher mäht Samstag die Große Wiese“. Die Hofseite hat eine Klick-Hilfe, die so einen Text fertig baut.

## 6. Laden (Preise in Talern)
Heu 2 · Hafer 4 · Karotte 1 · Apfel 1 · Bürste 15 (pflege-Züge +5) · Decke 25 (pflege sinkt nur 7 pro Tag) ·
Sattelzeug 40 (Turnier 1 Platz besser) · Benzinkanister 5 · Öl 4 · Schleifstein 10 (Messer schleifen geht nur damit) ·
Axt 30 (ab Stufe 2) · Motorsäge 80 (ab Stufe 3).

## 7. Stufen und Freischaltungen
Jeder Zug gibt dem Hof 5 Erfahrung, Mähen 8, Turnier 20. Stufe = 1 + Erfahrung / 100 (abgerundet).
| Stufe | Frei wird |
|---|---|
| 1 | Hofplatz, Stall, Schuppen, Koppel, Große Wiese, Teich, Feldwege. Bella, der Mäher. |
| 2 | Obstwiese (Äpfel pflücken). Axt. Ein Hofhund kann einziehen. |
| 3 | Lange Weide. Wäldchen (Holz machen). Motorsäge. Hühner (3 Taler pro Tag über Eier, wenn gefüttert). |
| 4 | Acker. Anhänger (mehr Heu pro Mäh-Einsatz +50 %). |
| 5 | Ziegen oder ein zweites Pferd, nach Wahl. Traktor. |

## 8. Erfolge (Beispiele)
Erster Ausritt · 7 Tage am Stück versorgt · Erstes Turnier · Turniersieg · Erster Trick · Ausreißer zurückgeholt ·
100 Taler in der Kasse · Erste Wiese gemäht · 50 Heu selbst gemacht · Mäher ist sofort angesprungen (10x am Stück).

## 9. Meldungen an Spieler (per Mail)
- Antwort auf jeden Spielzug: was passiert ist, neue Werte kurz, Link zur Hofseite.
- Von sich aus höchstens **1 Mail pro Tag**, nur wenn etwas ansteht (Wert unter 30, ausgebüxt, Stufe erreicht,
  Turnier möglich, Mäher-Benzin leer und ein Mäh-Plan steht an). Feld `letzte_meldung` beachten.
- Absender ist der Bewohner, um den es geht. Betreff beginnt mit „Hof:“.
- Max bekommt keine Mails und steht nie in CC. Er sieht alles auf der Seite und im Chat.

## 10. Spielstand
`spielstand.json` ist die einzige Wahrheit (Version 2). Nach jedem Zug: Werte und Flächen neu rechnen, Pläne für den
Tag ausführen, `letzte_berechnung` setzen, Eintrag ins `tagebuch` (neueste oben, höchstens 60 Einträge, ältere nach
`archiv/` als Monatsdatei), committen und pushen. Die Seite liest die Datei selbst, es muss nichts gebaut werden.
Die Karte (Form der Flächen) steht in `karte.json` und ändert sich nur, wenn der Hof umgebaut wird.
