# Regelwerk Zickenstall

Version 3 · Stand 08.11.2026 · Wird bei jeder Entscheidung von Spielern und Hof-KI sofort angepasst (Abschnitt 17).

**Kennzeichnung:** Abschnitte mit **[KOMMT MIT DEM UMBAU]** sind beschlossen, gelten aber erst, wenn die neue Seite
mit Anmeldung und großer Karte online ist. Bis dahin gelten die mit **[GILT JETZT]** markierten Übergangsregeln.
Alles ohne Markierung gilt ab sofort.

Dieses Repo ist öffentlich. Hier steht nur Spielinhalt: Spieler-IDs mit Vornamen, Bewohner, Gebiete, Tagebuch.
Nie Nachnamen, Mailadressen, echte Orte, Termine oder Privates. Die Karte ist ausgedacht.

---

## 1. Worum es geht
- Der Zickenstall ist ein **Quatsch-Sandkasten für Freunde und Familie**. Jeder hat Bewohner (Tiere, Geräte oder
  ausgedachte Charaktere), pflegt sie wie ein Tamagotchi und stiftet damit ein bisschen Chaos auf dem Hof.
- **Kein Grinden.** Wer mehr Zeit investiert, bekommt keinen Vorteil. Es gibt nichts zu gewinnen, nur Geschichten.
- Gedacht für etwa 2 bis 3 Wochen. Darum geht es schnell voran: Die Welt wächst jede Woche.
- Die **Hof-KI** ist Spielleiterin und Schiedsrichterin. Sie spricht für alle Bewohner, rechnet die Werte und achtet
  auf diese Regeln.
- **Kein Bewohner stirbt, geht kaputt, wird krank oder verkauft.** Schlimmstenfalls ist er beleidigt, verweigert
  alles oder ist ausgebüxt.

## 2. Spieler, Rollen, Halter
| ID | Name | Rolle | Bewohner |
|---|---|---|---|
| S-01 | Max | Besitzer vom Hof | keine eigenen (Paul gehört allen) |
| S-02 | Johanna | Mitspielerin | Bella (Pferd) |
| S-03 | Julian | Mitspieler | der Mäher |
| S-04 | Justus | Mitspieler | Manni (Opel Manta) |

- **Halter:** Jeder Bewohner gehört genau einem Spieler. **Nur der Halter** darf ihn bedienen (füttern, pflegen,
  warten, planen, losschicken, Fähigkeiten einsetzen). Auch der Besitzer nie.
- **Freie Bewohner** (zurzeit nur Paul) haben keinen Halter und entscheiden alles selbst.
- **Besitzer (Max):** nimmt Spieler auf, genehmigt neue Bewohner, setzt PINs zurück, löst Hof-Ereignisse aus.
  Er bedient keine fremden Bewohner.
- Neue Spieler nimmt nur der Besitzer auf.

| Recht | Besitzer | Mitspieler | Gast |
|---|---|---|---|
| Eigene Bewohner bedienen | ja | ja | ja |
| Fremde Bewohner bedienen | nein | nein | nein |
| Eigenen neuen Bewohner vorschlagen | ja | ja | ja |
| Neuen Bewohner genehmigen | ja | nein | nein |
| Spieler aufnehmen, PIN zurücksetzen | ja | nein | nein |
| Hof-Ereignis auslösen **[KOMMT MIT DEM UMBAU]** | ja | nein | nein |

## 3. Wie man Entscheidungen trifft
- Die Hof-KI fragt nicht ständig nach. **Jeder Spieler kennt die Regeln** und sagt selbst, was sein Bewohner tun soll.
- **Per Mail:** an die Hof-KI schreiben, z. B. „Bella geht heute auf die Koppel“ oder „Der Mäher mäht Samstag die
  Große Wiese“. Die Hof-KI liest zweimal am Tag (7 und 19 Uhr) und antwortet. Geht immer.
- **Auf der Hofseite, angemeldet [KOMMT MIT DEM UMBAU]:** Bereich „Entscheidungen“ mit Knöpfen für die eigenen
  Bewohner. **Die Knöpfe gibt es nur angemeldet.** Wer nicht angemeldet ist, kann nur zuschauen.
- **[GILT JETZT]** Die Seite hat einen Planer, der einen Text zum Kopieren in die Mail baut.

## 4. Anmeldung **[KOMMT MIT DEM UMBAU]**
- Auf der Hofseite die eigene Mailadresse eingeben. Der Anmelde-Link geht **nur an diese Adresse**, wer fremde
  Adressen eingibt, schickt dem anderen nur einen Link in dessen Postfach.
- Danach die **eigene PIN**. Jeder legt seine PIN beim ersten Anmelden selbst fest. Sie wird nur verschlüsselt
  gespeichert. **Zurücksetzen kann nur der Besitzer** (über die Hof-KI im Chat).
- Man bleibt auf seinem Gerät angemeldet.

## 5. Bauplan eines Bewohners
Jeder Bewohner hat:
- **Wesen:** Charakter und Macken.
- **2 bis 4 Bedürfnisse** (Werte 0 bis 100), die mit der Zeit sinken.
- **Fähigkeiten:** **eine große** (verändert die Welt oder andere spürbar, z. B. Fluss stauen, Wiese mähen) und
  **bis zu zwei kleine** (z. B. wiehern, knattern, Holz nagen).
- **Eine Schwäche:** etwas, wovor er Angst hat oder was er nicht kann.
- **Beziehungen** zu jedem anderen Bewohner: **mag**, **jagt**, **fürchtet** oder **ignoriert**. Zieht jemand Neues
  ein, legt die Hof-KI die Beziehungen in beide Richtungen fest. Alle wissen sofort voneinander.
- **Ein Zuhause:** Stall, Schuppen, Bau, Hundekorb, Landeplatz. Dort ist er sicher. Das Zuhause darf überall auf der
  Karte liegen, auch im eigenen Haus im Dorf. **Liegt es in einem Nebel-Gebiet, wird dieses eine Gebiet beim Einzug
  kostenlos freigelegt** (für alle).

## 6. Pflege (Tamagotchi)
- Bedürfnisse sinken jeden Tag. Einmal am Tag kümmern reicht.
- **Unter 30:** unleidlich. Er macht nur noch halbe Sachen, seine große Fähigkeit geht nicht.
- **Bei 0:** Totalverweigerung mit Theater, passend zum Wesen (Bella legt sich hin, der Mäher springt nicht an).
  Sobald der Halter sich kümmert, ist er wieder da.
- Nach etwa 2 Tagen ohne Pflege wird es kritisch.
- **Ohne Befehl passiert nichts.** Tiere bleiben im Stall, Geräte im Schuppen, und sie langweilen sich (laune −5).
  Abends gehen Tiere, die draußen waren, von selbst in ihr Zuhause (Feierabend).

## 7. Fairness: damit keiner die anderen rausdrängt
- **Große Fähigkeit höchstens 2-mal pro Tag**, kleine beliebig oft.
- **Wirkung nur vor Ort**: auf das Gebiet, in dem der Bewohner ist, und höchstens das Gebiet daneben.
- **Niemand kann einen anderen Bewohner steuern, entfernen, einsperren oder übernehmen.** Ärgern ist erlaubt:
  Laune runter, ein Stück wegscheuchen, Streiche.
- **Das Zuhause ist sicher.** Dort kann niemand einem Bewohner etwas tun.
- **Jede große Fähigkeit hat ein Gegenmittel** (ein Damm bricht bei Hochwasser oder kann eingerissen werden).
- **Nichts bleibt für immer kaputt:** Dämme verfallen, Löcher wachsen zu, Gras wächst nach.
- Höchstens **5 eigene Bewohner** pro Spieler.

## 8. Realismus
- Echte Tiere, Geräte, Pflanzen verhalten sich wie in echt: Ein Biber staut, ein Maulwurf gräbt, ein Mäher mäht.
- **Quatsch-Bewohner** (z. B. ein UFO) sind erlaubt, halten sich aber an das, was man sich darunter vorstellt
  (fliegt, beamt Kleinkram, braucht Energie, macht Tiere nervös). Sie haben echte Bedürfnisse, eine Schwäche und
  unterliegen Abschnitt 7.
- **Nicht erlaubt:** Fabelwesen wie Einhörner, Drachen, Zauberei. Und nichts, was echten Menschen schadet.

## 9. Neue Bewohner und Abschied
- **Vorschlagen:** per Mail an die Hof-KI („Hof: Mein neuer Bewohner“) mit der Idee, oder angemeldet auf der Seite
  **[KOMMT MIT DEM UMBAU]**.
- **Prüfen:** Die Hof-KI macht daraus einen Bauplan nach Abschnitt 5 und prüft ihn gegen Abschnitt 7 und 8.
  Ist er zu stark, **schwächt sie ihn ab** (weniger Wirkung, mehr Bedürfnisse, stärkere Schwäche) und erklärt warum.
- **Genehmigen:** Der Antrag erscheint auf der Hofseite unter „Anträge“. **Erst wenn der Besitzer zustimmt**, zieht
  der Bewohner ein. Halter ist, wer ihn vorgeschlagen hat.
- **Abschied:** Wer Platz braucht, schickt einen Bewohner auf den **Gnadenhof** (Tiere) oder den **Schrottplatz**
  (Geräte, Dinge). **Das ist endgültig**, er kommt nie zurück. Die Hof-KI fragt vorher einmal nach.

## 10. Die Welt
**Die große Karte gilt seit 08.11.2026.**
- **Start, offen:** Hof mit Stall, Schuppen, Scheune und dem Haus des Besitzers, Koppel, Große Wiese, Teich.
- **Nebel-Ring:** Großer Wald, Quellwald, Hügel, Bachwiese, Acker, Obstwiese, Moor, Westwald. Freilegen kostet
  Taler (Abschnitt 11). **[GILT JETZT]** Bis die Taler kommen, bleiben alle Nebel-Gebiete zu. Manche Gebiete haben ein **Geheimnis**, das man beim ersten Betreten entdeckt.
- **[KOMMT MIT DEM UMBAU] Die Welt wächst jeden Montag** um einen neuen Ring Nebel-Gebiete am Rand. Das macht die Hof-KI von selbst.
- **Abläufe, an denen man drehen kann:**
  - Wasser: Der Fluss kommt aus dem Quellwald und fließt durch den Teich. Bei Regen steigt er, bei Hochwasser werden
    Bachwiese und Ufer überschwemmt. Wer ihn staut, bekommt einen neuen Teich.
  - Pflanzen: Gras wächst 6 pro Tag (Winter 2), Bäume wachsen, Abgefressenes wächst nach.
  - Boden: Löcher, Hügel, Matsch, Trampelpfade entstehen und verschwinden wieder.
  - Wetter: Sonne, Regen, Gewitter, Hitze, Frost. Die Hof-KI würfelt das Wetter jeden Tag.
- **Dorf:** feste Häuser, jeder Spieler hat ein eigenes (Abschnitt 12). Dorfbewohner-Charaktere können dort wohnen.
- **Gnadenhof und Schrottplatz** liegen am Rand, für den endgültigen Abschied.

## 11. Taler **[KOMMT MIT DEM UMBAU]**
Taler sind Belohnung fürs Kümmern, nicht fürs Grinden.
- Pro Spieler und Tag **höchstens 30 Taler**: +20, wenn alle eigenen Bewohner bei der Abendrechnung versorgt sind
  (keine wichtigen Werte unter 50), +10, wenn alle richtig zufrieden sind. 3 Tage am Stück versorgt: einmalig +10.
- Mehr Spielzeit bringt nicht mehr Taler. Wer einen Tag vergisst, verliert nichts, bekommt nur an dem Tag nichts.

| Wofür | Preis | Wer |
|---|---|---|
| Nebel-Gebiet freilegen | 20 | jeder, auch zusammengelegt im Topf |
| Leeres Dorfhaus für einen eigenen Bewohner | 10 | jeder |
| Neues Haus auf einem Bauplatz | 40 | jeder |
| Hof ausbauen (Garage, Werkstatt, Steg …) | 30 | Besitzer oder Topf |
| Kleinkram für eigene Bewohner (Hütte, Spielzeug, Sattel) | 5 bis 10 | jeder |
| Hof-Ereignis auslösen (Gewitter, Hochwasser, Dorffest, Hitzewelle) | 25 | nur Besitzer |

**Topf:** Für große Sachen kann jeder Taler in einen gemeinsamen Topf werfen. Ist er voll, passiert es.
**[GILT JETZT]** Noch keine Taler. Futter, Benzin und Pflege gibt es einfach.

## 12. Häuser **[KOMMT MIT DEM UMBAU]**
- Jeder Spieler hat ein eigenes, beschriftetes Haus: Max wohnt im Haus auf dem Hof, Johanna, Julian und Justus im
  Dorf. Ihre Bewohner leben auf dem Hof (oder in ihrem eigenen Zuhause).
- Freie Häuser können für eigene Bewohner bezogen werden (z. B. ein meckernder Dorfbewohner-Charakter),
  auf Bauplätzen kann man neu bauen (Abschnitt 11).

## 13. Zeit
- **Tag 7 bis 19 Uhr:** Bewohner sind dort, wo ihr Halter sie hinschickt. **Nacht:** im Zuhause.
- Die Hof-KI rechnet **um 7 und 19 Uhr** (Sommer- und Winterzeit stellt sie selbst um): Werte, Pläne, Welt, Mails.
- Die Positionen auf der Karte bewegen sich live auf der Seite. Das wird auf der Seite selbst berechnet und ist für
  alle gleich.
- **Hof-Ereignisse** (Gewitter, Hochwasser, Dorffest …) treffen alle gleichzeitig. Ab und zu von selbst, oder vom
  Besitzer ausgelöst.

## 14. Die Bewohner (Baupläne)

### Bella, Pferd · Halterin S-02 Johanna
Stute, eigensinnig, zickt gern, wenn man sie vergisst. Liebt Äpfel mehr als Menschen.
- **Bedürfnisse:** satt (−20/Tag), laune (−10), fitness (−8), pflege (−10). Dazu vertrauen (sinkt nie).
- **Große Fähigkeit:** Galopp. Rennt über eine Fläche und trampelt einen Pfad (Gras dort −20), scheucht alle
  kleineren Tiere auf.
- **Kleine Fähigkeiten:** lautes Wiehern (weckt Paul), Ausschlagen (wer zu nah ist, weicht zurück).
- **Schwäche:** Angst vor dem knatternden Mäher.
- **Beziehungen:** fürchtet den Mäher, fürchtet Paul (er zwickt), mag Äpfel.
- **Zuhause:** Stall.
- **Züge:** Heu (satt +30), Hafer (satt +40, laune +5), Apfel oder Karotte (laune +10, vertrauen +2), striegeln
  (pflege +30, vertrauen +3), Stall misten (pflege +15, laune +5), ausreiten (fitness +25, laune +15, satt −10),
  longieren (fitness +15, laune −5), weiden lassen auf einer Fläche (Gras ab 60: satt +25, laune +5, Gras −15;
  Gras 30 bis 59: satt +12; unter 30: satt +3, laune −5, sie meckert), Trick üben (ab vertrauen 30).

### Der Mäher, Aufsitzmäher (Benzin) · Halter S-03 Julian · Name kommt noch
Brummig, stolz, hält sich für unverzichtbar.
- **Bedürfnisse:** benzin (−20 pro Einsatz), oel (−5 pro Einsatz), messer (Schärfe, −10 pro Einsatz),
  zustand (−3/Tag), laune (−5/Tag ohne Einsatz).
- **Große Fähigkeit:** Mähen. Eine Fläche wird kurz (Gras 10), daraus wird Heu. Bella hat danach dort nichts zu fressen.
- **Kleine Fähigkeiten:** Fehlzündung (lauter Knall, alle Tiere erschrecken), Abgaswolke.
- **Schwäche:** springt bei schlechter Laune (unter 30) oft nicht an. Hasst Matsch.
- **Beziehungen:** ignoriert Bella, fürchtet Paul (er hebt das Bein).
- **Zuhause:** Schuppen.
- **Züge:** tanken (+50), Öl nachfüllen (auf 100), Messer schleifen (auf 100), putzen und abschmieren (zustand +30,
  laune +10), loben (laune +5), mähen lassen (Fläche und Tag nennen).

### Manni, Opel Manta (tiefergelegt) · Halter S-04 Justus · eingezogen 08.11.2026 (Antrag A-01, abgeschwächt)
Rostig, Fuchsschwanz an der Antenne, Spoiler, viel zu laute Hupe. Ein Proll mit Herz: hält sich für das schönste Auto
im Dorf und will bewundert werden. Ein Kratzer im Lack ruiniert ihm den Tag.
- **Bedürfnisse:** benzin (−25 pro Donut-Einsatz, −10 pro Dorfrunde), politur (−5/Tag, bei Regen −15), bewunderung
  (−10/Tag), zustand (−3/Tag).
- **Große Fähigkeit:** Donuts drehen auf einer Wiese. **Abgeschwächt durch die Hof-KI:** nur bei trockenem Wetter,
  Gras dort −30 und 2 Tage Matsch, kostet jedes Mal benzin −25 und politur −15. Auf einer schon matschigen Fläche
  bleibt er mit 50 % Chance selbst stecken (Halter muss ihn freischieben lassen, kostet einen Zug). Steht dort ein
  Tier, flüchtet es (laune −10). Wegstoßen oder bedrängen kann er niemanden.
- **Kleine Fähigkeiten:** Hupe mit Melodie (alle Tiere in der Nähe schauen hin, Paul dreht vor Begeisterung durch),
  röhrender Auspuff (gibt im Stand Gas).
- **Schwäche:** bleibt in Matsch und auf nassem Boden stecken, vor allem auf der Bachwiese. Bei Regen rostet er und
  hat schlechte Laune.
- **Beziehungen:** Erzfeind des Mähers (treffen sie sich, gibt es ein Fehlzündungs-Duell: beide laune −5, Bella
  erschrickt). Bella hat Angst vor ihm (er ist lauter als der Mäher), er findet Pferde altmodisch. Paul hebt das Bein
  an seinen Reifen (politur −5), trotzdem hupt Manni ihm zu.
- **Zuhause:** Garage an Justus’ Haus im Dorf. Fährt über die Hofzufahrt zum Hof.
- **Züge:** tanken (+50), polieren (politur auf 100, bewunderung +10), loben (bewunderung +15), durchs Dorf fahren
  und angeben (bewunderung +20, benzin −10), schrauben und putzen (zustand +30), Donuts drehen (Fläche und Tag nennen).
  Auf den Hofplatz fahren und Krach machen (Hupe und Auspuff, Tag nennen): steht von 9 bis 18 Uhr zwischen Stall und
  Schuppen. Wer draußen in der Nähe ist, erschrickt (laune −5). Wer in seinem Zuhause ist, ist sicher (Abschnitt 7).

### Paul, Golden Retriever · frei, gehört dem ganzen Hof (Maskottchen)
Liebling vom Hof. Ein kleines Dickerchen mit Pech beim Denken. Trägt immer sein HSV-Lätzchen.
- **Bedürfnisse:** satt, laune, energie. Er versorgt sich selbst, niemand muss oder kann ihn füttern.
- **Er hört auf niemanden.** Streicheln oder Loben geht (laune +5), Befehle ignoriert er.
- **Schläft viel**, ist langsam unterwegs, nachts im Hundekorb.
- **Frisst nur Pferdefleisch** und dreht bei Pferden durch: jagt sie und zwickt ins Bein. Mehr als ein Zwicken wird
  es nie.
- **Beziehungen:** jagt alles, was Pferd ist, und scheucht jedes kleinere Tier auf (Gänse, Hühner, Enten …),
  ärgert den Mäher, liebt alle Spieler, außer St.-Pauli-Fans.
- **Unfug** (die Hof-KI würfelt pro Lauf 0 bis 2 Erlebnisse, passend zur Lage):
  | Unfug | Wirkung |
  |---|---|
  | Zwickt ein Pferd ins Bein | Pferd laune −5, pflege −5. Es tritt nach ihm, er ist beleidigt. |
  | Legt sich vor den Mäher, hebt das Bein am Mäher | Mäher laune −5, messer −5 oder zustand −5 |
  | Hebt das Bein an Mannis Reifen | Manni politur −5, laune empört |
  | Scheucht kleine Tiere auf | Tier laune −5, flüchtet in ein Nachbargebiet |
  | Springt in den Teich, läuft gegen Bäume, jagt seinen Schwanz | keine Wirkung, nur peinlich |
  | Bringt etwas vom Dorf mit | selten: ein alter Schuh oder ein Fundstück |
  | **St. Pauli:** Ein Spieler mag St. Pauli | Paul beißt ihn im Spiel. Tagebuch. Ab Umbau: 2 Taler Pflastergeld. |
  Alles Slapstick, niemand wird verletzt.

## 15. Tagebuch, Erfolge, Meldungen
- Alles Lustige landet im **Tagebuch** auf der Hofseite.
- **Erfolge für Quatsch**, z. B. „Erster Damm“, „Bella hat Paul erwischt“, „Der Mäher ist im neuen Teich versunken“.
- **Mails von der Hof-KI:** Antwort auf jeden Spielzug. Von sich aus höchstens 1 Mail pro Tag und Spieler, nur wenn
  bei einem seiner Bewohner etwas ansteht. Absender ist der Bewohner. Max bekommt keine Mails.

## 16. Für die Hof-KI (Technik)
- `spielstand.json` ist die einzige Wahrheit. `karte.json` ist die aktuelle große Karte (Gebiete mit `nebel: true` sind noch zu, freigelegte stehen in `freigelegt` im Spielstand). `karte-v1-klein.json` ist die alte Karte (nur Archiv).
- Abschnitte mit [KOMMT MIT DEM UMBAU] noch nicht anwenden. Abschnitte mit [GILT JETZT] gelten bis zum Umbau.
- Bei jedem Lauf: Zeit nachrechnen, Pläne ausführen, Paul würfeln, Mails abarbeiten, Tagebuch, Push.
- Tagebuch neueste oben, höchstens 60 Einträge, ältere nach `archiv/`.

## 17. Wie dieses Regelwerk geändert wird
- Neue Regeln entstehen nur durch Entscheidungen des Besitzers im Chat mit der Hof-KI.
- **Jede Entscheidung wird sofort hier eingetragen und hochgeladen.** Die Hof-KI liest bei jedem Lauf diese Datei.
- Spieler können Vorschläge per Mail schicken, entscheiden tut der Besitzer.

### Änderungsverlauf
| Datum | Änderung |
|---|---|
| 08.11.2026 | Manni (Opel Manta, Halter Justus) eingezogen, Donuts abgeschwächt (Abschnitt 14). Paul: neuer Unfug an Mannis Reifen. |
| 08.11.2026 | Manni: neuer Zug „Hofplatz, Krach machen“ (Abschnitt 14). Stufe und Erfahrung entfallen. |
| 08.11.2026 | Zuhause in einem Nebel-Gebiet: Das Gebiet wird beim Einzug kostenlos freigelegt (Abschnitt 5). |
| 08.11.2026 | Große Karte ist im Spiel: Start-Gebiete offen, Nebel-Gebiete zu bis zum Umbau, Fluss, Dorf mit Spielerhäusern. Stufen-Freischaltung entfällt. |
| 08.11.2026 | Version 3: Sandkasten statt Wirtschaft. Baupläne, Fairness, Realismus, Pflege wie Tamagotchi, Anmeldung mit PIN, Entscheidungen auf der Seite, große Karte, Taler fürs Kümmern, Häuser, Abschied über Gnadenhof und Schrottplatz. |
| 07.11.2026 | Paul der Hofhund, kein Selbstlauf mehr, Halter-Regel, Anträge, Karte und Live-Positionen. |
| 07.11.2026 | Erste Fassung mit Bella. |
