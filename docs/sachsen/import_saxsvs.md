# Import von Daten aus SaxSVS nach Magellan

1. [Beachten Sie bitte die Mindestvoraussetzungen für den Import](einstieg.md/#voraussetzungen-fur-den-import)
2. Lesen Sie in diesem Abschnitt wie Sie mit Meldungen durch den Import umgehen.
3. Lesen Sie im Abschnitt [Schnittstellendatei nach Magellan importieren](#schnittstellendatei-nach-magellan-importieren), wie Sie den Import durchführen.

## Prüfung von Schülerdaten

Beim Import wird eine zweistufige Prüfung durchgeführt.

Stufe 1:
Es wird geprüft, ob sich bereits ein Schüler mit gleicher GUID in Magellan befindet. Wenn dies der Fall ist, wird dieser Schüler  nicht erneut importiert.

Stufe 2:
Es wird zusätzlich geprüft, ob sich der zu importierende Schüler bereits in Magellan befindet, es aber keine Übereinstimmung mit der GUID gibt.

Dieser Fall wird anhand folgender Felder geprüft:

* Vorname (muss identisch sein)
* Nachname (muss identisch sein)
* Geburtsdatum (muss identisch sein)
* IDIntern (muss leer sein)

Wird ein Schüler als bereits in Magellan vorhanden erkannt, wird er importiert, erhält aber zusätzlich einen Eintrag im Feld IDIntern mit der ID des gefundenen Stammschülers. Dieser Schüler wird anschließend genau wie ein Nebenschüler behandelt, wird er im selben Zeitraum wie der Stammschüler eingeschult, ergeben sich zwei Schüler, die über die IDIntern verbunden sind, damit gleiche Stammdaten haben. Wird der Nebenschüler in einem anderen Halbjahr eingeschult, als der Stammschüler gefunden wurde, werden Neben- und Stammschüler zusammengeführt.

!!! warning "Wichtig"

    Wir gehen wie oben beschrieben vor, um den Import im Falle einer Neubewerbung eines Stammschülers zu ermöglichen. Sollten Sie versehentlich die Schüler erneut imporiert haben und keine Nebenlaufbahn des Schülers wünschen, löschen Sie die importierten Schüler bitte heraus.

!!! info "Hinweis"

    Ob in Ihrer Importdatei Schüler als bereits vorhanden erkannt werden, können Sie mithilfe der Option "Daten prüfen" durch den Importassistenen vorab prüfen lassen.

### GUID - Was muss bei importierten Schülern beachtet werden

Erst einmal allgemein: Jeder Schüler hat eine sogenannte GUID, die den Schüler mit seiner Ausbildung kennzeichnet. Wechselt der Schüler in einen anderen Bildungsgang (Beispiel: vom Bäcker zum Erzieher), wird auch die GUID geändert.

Ein Beispiel:
Absolviert ein Schüler eine Ausbildung als Bäcker an Schule 1 und wechselt anschließend für eine Ausbildung als Erzieher an Schule 2, erhält der Schüler eine neue GUID - **diese wird innerhalb von SaxSVS vergeben, nicht in Magellan**. 

!!! danger "Achtung"

    Damit die importierten Schüler beim späteren Übertrag nach SaxSVS wiedererkannt werden können, darf die GUID nicht innerhalb von Magellan geändert werden. Wird die GUID auf der Ausbildungskarte geändert, wird der Schüler als weiterer Datensatz nach SaxSVS übergeben, als Ergebnis erscheint der Schüler in SaxSVS doppelt.

## Prüfung von Betriebedaten der Ausbildung

***Groß- und Kleinschreibung ist bei der Prüfung nicht relevant.***

Es ist möglich, das sich zu importierende Einstellungs- und Ausbildungsbetriebe bereits in Magellan befinden. Da es über verschiedene Schulen hinweg keine Möglichkeit gibt Betriebe eindeutig zu identifizieren, muss man über verschiedene Merkmale eines Betriebes versuchen diesen in Magellan zu identifizieren um ggf. Dopplungen im System vermeiden.

Für Betriebe prüft der Importmechanismus folgende Magellan-Felder:

* Name 1
* PLZ
* Ort

Es wird der einzuspielende Betrieb mit den Datensätzen in Betriebe nach diesen Kriterien geprüft. Wird ein Betrieb gefunden, der exakt die gleichen Werte in den Feldern aufweist, dann gehen wir vom gleichen Betrieb aus und nutzen diesen als Verweis für den jeweiligen Schüler.

## Prüfung von Sorgeberechtigen

***Groß- und Kleinschreibung ist bei der Prüfung nicht relevant.***

Es ist möglich, das sich zu importierende Sorgeberechtige bereits in Magellan befinden, z.B. beim Import eines Geschwisterkindes, oder weil der Schüler schon einmal an Ihrer Schule war oder sich beworben hat und die Sorgeberechtigen noch in Ihrer Datenbank sind. Da es über verschiedene Schulen hinweg keine Möglichkeit gibt Sorgeberechtigte eindeutig zu identifizieren, muss man über verschiedene Merkmale eines Sorgeberechtigten versuchen diesen zu identifizieren um ggf. Dopplungen im System vermeiden.

Für Sorgeberechtigte prüft der Importmechanismus folgende Magellan-Felder:

* Vorname
* Nachname
* PLZ
* Ort

Es wird der einzuspielende Sorgeberechtigte mit den Datensätzen in Sorgeberechtite nach diesen Kriterien geprüft. Wird ein Sorgeberechtigter gefunden, der exakt die gleichen Werte in den Feldern aufweist, dann gehen wir vom gleichen Sorgeberechtigten aus und nutzen diesen als Verweis für den jeweiligen Schüler.

Werden mehrere Datensätze gefunden wird zusätzlich die `Strasse` geprüft, einmal gesamt und wenn dies nicht zum Erfolg führt, dann werden noch einmal nur die ersten 5 Zeichen der `Strasse` geprüft.
Wenn nach diesen Prüfungen ein Datensatz übrig bleibt, dann wird dieser genommen.

## Zuordnung zu einer Klasse

Die Schüler sind nach dem Import nach Magellan nicht einer Klasse zugeordnet (sondern Vagabunden), auch wenn sie in SAXSVS bereits einer Klasse zugeordnet sind.
Die SAXSVS-Klasse wird als Wert ins Verzeichnis `Einschulmerkmale` übernommen und für die Vagabunden ins Feld `Einschulmerkmale3` übertragen. Dieses Feld wird unter `Laufbahnprozesse > Schüler einschulen` als Zuordnungshilfe gezeigt.

## Mit Meldungen des Imports umgehen

Meldungen die durch die Mindestprüfung der Kataloge entstehen. Jeder Schlüssel wird geprüft, aber nur beim ersten Schüler in dem der Schlüssel fehlt schlägt die Meldung an, um Massenmeldungen aufgrund eines fehlenden Schlüssel zu unterbinden. Da ein Schüler nicht importiert wird, wenn dieser den fehlenden Schlüssel einsetzt, kann es sein, dass von dieser Meldung mehrere Schüler betroffen sind und diese nicht eingelesen werden.

`Im Schlüsselverzeichnis fehlt der Schlüssel "Schlüsselwert" - Dieser Schüler "Max Mustermann" - und ggf. weitere werden übersprungen.`

Meldungen die zu Ihrer Information dienen, z.B. um ggf. Falschzuweisungen, die nur Sie entdecken können, im Nachgang korrigieren zu können.

Import von           | Meldung
-------------------- | -------
**Betriebe**         | Für den Schüler "Max Mustermann" wurde der `[Einstellungsbetrieb/Praxisbetrieb]` "Musterbertrieb" (Id) gefunden.<br>Dieser wird mit dem Schüler verbunden.
**Sorgeberechtigte** | Für den Schüler "Max Mustermann" wurde der Sorgeberechtigte "Papa Mustermann" (Id) gefunden.<br>Dieser wird mit dem Schüler verbunden.
**Sorgeberechtigte** | Für den Schüler "Max Mustermann" wurden mehrere Sorgeberechtigte entsprechend der Namen (PLZ und Ort) gefunden. Bei weiterer Prüfung der Strasse konnte keine Übereinstimmumg festgestellt werden.<br>Für diesen Schüler wird der Sorgeberechtigte neu angelegt und verbunden.
**Schüler**          | Es existiert bereits der Schüler "Max Mustermann" mit der zu importierenden GUID "`Eine GUID`"
**Schüler**          | Dem Schüler ["Max Mustermann"] fehlen folgende Mindestangaben:<br>- Keine GUID<br>- Kein Vorname<br>- Kein Nachname<br>- Kein Geburtsdatum<br><br>**Oder Varianten dieser Meldung**
**Schlüssel**        | Es konnte kein Datensatz in der Tabelle "Tabellenname" anhand des Schlüssels "Schlüsselwert" gefunden werden. Dies bedeutet, dass ein Schlüssel für ein Feld in der Datenbank beim Import nicht gesetzt werden konnte, da der Schlüssel im entsprechenden Katalog nicht vorhanden ist. Dies ist eine Meldung, die aufgrund der Mindestprüfung nicht auftauchen sollte.

Meldungen die sie eigentlich **nie** sehen sollten, da diese nicht auftreten dürften. Diese Bedürfen einer Meldung im STÜBER-Ticketsystem. In den meisten Fällen wird der nicht importierte Datensatz übersprungen und der Import weiter ausgeführt. Aufgrund der Meldungen können Sie ggf. nicht importierte Daten manuell im System eintragen.

Import von                   | Meldung
---------------------------- | -------
**Betriebe**                 | Es ist ein Fehler beim Einfügen des Betriebs für den Schüler "Max Mustermann" aufgetreten.<br>Der Betrieb "Musterbetrieb" konnte nicht importiert werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.<br><br>Fehler: `Eine Systemfehlermeldung` | Der Betrieb konnte nicht nach Magellan eingespielt werden. Die Fehlermeldung sollte einen Hinweis auf den Grund geben.
**Betriebe**                 | Es ist ein Fehler beim Einfügen des Betriebs für den Schüler "Max Mustermann" aufgetreten.<br>Die Id des Betriebs "Musterbetrieb" wurde nicht zurückgeliefert.
**Schüler**                  | Es ist ein Fehler beim Einfügen des Schülers "Max Mustermann" aufgetreten.<br>Der Schüler konnte nicht importiert werden. Der Schüler wird übersprungen und der Vorgang wird fortgesetzt.
**Schüler-Förderung**        | Es ist ein Fehler beim Einfügen der Schüler-Förderung für den Schüler "Max Mustermann" aufgetreten.<br>Die Förderung:<br>- Bedarf: Ein Förderbedarf`<br>- Schwerpunkt1: Förderschwerpunkg 1<br>- Schwerpunkt2: Förderschwerpunkt 2<br>- Behinderung: Behinderungsart<br>konnte nicht importiert werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.`;
**Sorgeberechtigte**         | Es ist ein Fehler beim Einfügen des Sorgeberechtigten für den Schüler "Max Mustermann" aufgetreten.<br>Der/Die Sorgeberechtigte "Maria Mustermann" konnte nicht importiert werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.
**Schüler-Sorgeberechtigte** | Es ist ein Fehler beim Einfügen des Schueler-Sorgeberechtigten für den Schüler "Max Mustermann" aufgetreten. Der/Die Sorgeberechtigte "Maria Mustermann" konnte nicht importiert werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.
**Schüler-Ausbildung**       | Es ist ein Fehler beim Einfügen der Schüler-Ausbildung für den Schüler "Max Mustermann" aufgetreten.<br>Die Ausbildung "`Bildungsgang`" konnte nicht importiert werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.
**Aktuelle Ausbildung**      | Es ist ein Fehler beim Setzen der aktuellen Schueler-Ausbildung für den Schüler "Max Mustermmann" aufgetreten.<br>Die Ausbildung "`Bildungsgang`" konnte nicht gesetzt werden. Der Datensatz wird übersprungen und der Vorgang wird fortgesetzt.

## Schnittstellendatei nach Magellan importieren

Sie importieren die im [Einstieg](einstieg.md#einfuhrung) erwähnte XML-Datei aus SaxSVS. Das Ergebnis des Imports sind Vagabunden in der Ansicht "Schüler" mit den dazugehörigen Sorgeberechtigen, Schüler-Förderungen und Schüler-Ausbildung.

## Import ausführen

Für den Import der Schnittstellendatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Extras` auf und wählen den Unterpunkt `Import`.
![Daten nach Magellan importieren über `Schüler > Importe > Import...`](/assets/images/sachsen/import.saxsvs01.png)<br><br>

Es startet der Importassistent, bitte wählen Sie die Schnittstelle `SAX-SVS (BBS)` aus.
![Wählen Sie die Schnittstelle aus!](/assets/images/sachsen/import.saxsvs02.png)<br><br>

Fügen Sie über das Plus die zu importierende SAXSVS.XML hinzu.
![Wählen Sie die Schnittstelledatei aus!](/assets/images/sachsen/import.saxsvs03.png)<br><br>

Im unteren Bereich geben Sie an, ob Sie die zu importierende Datei vorab prüfen möchten, die Prüfung und Import zusammen durchführen, oder ohne Prüfung den Import ausführen möchten.
![Wählen Sie die Art des Imports aus!](/assets/images/sachsen/import.saxsvs04.png)<br><br>

Starten Sie den Import oder die Prüfung per Klick auf `Fertigstellen`!
![Starten Sie den Import!](/assets/images/sachsen/import.saxsvs05.png)

## Mögliche Probleme

Sollte Ihnen in der Auswahl im Exportassistenten nicht der Punkt `SAXSVS` gezeigt werden, ist vermutlich im Willkommensassistenten nicht die Bundeslandauswahl "Sachsen" getroffen worden.

### So geht`s

1. Schließen Sie bitte Magellan und starten Sie bitte den Magellan Administrator und wechseln in den Menüpunkt `Datenbankverbindungen`.
2. Klicken Sie doppelt auf Ihre Verbindungszeile, es öffnet sich das Fenster `Verbindungsdetails`.
3. Rufen Sie den Punkt `Datenbank` auf und tragen im Feld `Region` "Sachsen" ein.<br>Im Anschluss starten Sie Magellan wieder, unter `Extras > Importe > Import...` sollte jetzt auch die Auswahl `SAXSVS` zur Verfügung stehen!

## Was wird importiert

### Schüler

Feld in Magellan|Feld in der Schnittstelle|Verzeichnis
--|--|--
`Magellan > Schüler > Daten 1 > Vorname|`an_vname`|-|
`Magellan > Schüler > Daten 1 > Nachname` | `an_name`|-
`Magellan > Schüler > Daten 1 > Geburtsname` | `an_gebname`|-
`Magellan > Schüler > Daten 1 > Geburtsdatum` | `an_gebdat`|-
`Magellan > Schüler > Daten 1 > Geburtsort` | `an_gebort`|-
`Magellan > Schüler > Daten 1 > PLZ` | `an_plz`|-
`Magellan > Schüler > Daten 1 > Ort` | `an_ort`|-
`Magellan > Schüler > Daten 1 > Ortsteil` | `an_ortsteil` |-
`Magellan > Schüler > Daten 1 > Strasse` | `an_strasse`|-
`Magellan > Schüler > Daten 1 > Land` | `an_staat`|-
`Magellan > Schüler > Daten 1 > Gemeinde` | `PLZ, Ort`|-
`Magellan > Schüler > Daten 1 > Staatsang1` | `an_staatsang_1`| `Staatsangehoerigkeiten`
`Magellan > Schüler > Daten 1 > Staatsang2` | `an_staatsang_2`| `Staatsangehoerigkeiten`
`Magellan > Schüler > Daten 1 > NichtDeutscheHerkunft` | `an_migr_grund`|- 
`Magellan > Bewerber > Daten 1 >Einschulmerkmal3`|`al_laufb_kl`|-
`Magellan > Schüler > Daten 2 > Überweisung > Einschulantrag/Ausnahme` | `al_ausgen`|-
FFoerderung | `al_laufb_bgut`|-
`Magellan > Schüler > Daten 3 > 1. Fremdsprache 1` | `al_fremd_fs1`| `Faecher`
`Magellan > Schüler > Daten 3 > 1. Fremdsprache 2` | `al_fremd_fs2`| `Faecher`
`Magellan > Schüler > Daten 3 > 1. Fremdsprache 3`| `al_fremd_fs3`| `Faecher`
FHAbschlussABSSchulform | `av_abs_schart`|  `SchulformenHerkunft`
FHAbschlussABS | `av_abs_zeugnis`|  `AbschluesseExtern`
FHAbschlussBBSSchulform | `av_bbs_schart`|  `SchulformenHerkunft`
FHAbschlussBBS | `av_bbs_zeugnis`|  `AbschluesseExtern`
FMerkmalU2 | `an_migr_dat`|- 
FMerkmalS1 | `al_status`| `SchuelerMerkmale`

### Daten4 > Beeinträchtigungen und Fördermaßnahmen

Feld in Magellan|Feld in der Schnittstelle|Verzeichnis
--|--|--
Daten4 > Beeinträchtigungen und Fördermaßnahmen<br/>als eine Zeile|`af_behart`=> Behinderung/Diagnose<br/>`al_mfoerdersw`=>Förderschwerpunkt1<br/>`an_migr_daz3`=>Fördermaßnahme/Bedarf|`Behinderungsarten`<br/>`FoerderSchwerpunkte`<br/>`J` ergibt `DAZ-3`
Daten4 > Beeinträchtigungen und Fördermaßnahmen<br/>als eine Zeile|`af_schwaeche` => Förderschwerpunkt2<br/>`af_schwaeche_dat`=>Von|`FoerderSchwerpunkte`
Daten4 > Beeinträchtigungen und Fördermaßnahmen<br/>(ggfs. als mehrere Zeilen)|Bedarf=> `af_int`<br/>Schwerpunkt1=>`af_int_foerdersw`<br/>Von =>`af_int_von`<br/>Bis =>`af_int_bis`<br/>tunden1 =>`af_int_rs_std`<br/>Stunden2 =>`af_int_fs_std`| SopaedFoerderungen<br/>FoerderSchwerpunkte<br/>-<br/>-<br/>-<br/>-

### Sorgeberechtigte

Feld in Magellan|Feld in der Schnittstelle|Verzeichnis
--|--|--
Sorgerecht| `as_berechtigt`|-
Verhaeltnis| `as_beziehung`|-
Anrede    | `as_anrede`|-
Vorname   | `as_vname`|-
Nachname  | `as_name`|-
Land      | `as_land`|-
PLZ       | `as_plz`|-
Ort       | `as_ort`|-
Ortsteil  | `as_ortsteil`|-
Strasse   | `as_strasse`|-

### Schüler > Ausbildung

Feld in Magellan|Feld in der Schnittstelle|Verzeichnis
--|--|--
GUID   | `schueler extern_id`|-
Schulform    | `al_schulart`|Schulformen
Organisation   | `al_zeitform`|Organisationen
Bildungsgang | `al_kennziffer`|Bildungsgaänge
Neuanfaenger | `al_laufb_neuanf`|-
AusbildungBis| `al_abschl_dat`|-

### Folgende Knoten werden nicht importiert

Feld in der Schnittstelle|Anmerkung
--|--    
`<al_zeitform>` | Organisation der Klasse: Da der Schüler als Vagabund importiert wird, kann der Wert nicht importiert werden.
`<al_laufb_von>` | Kann erst mit Einschulung gesetzt werden
`<al_laufb_bis>` | Ende der Klasse (kann noch nicht feststehen)
`<al_laufb_bem>` | Keine Entsprechung in Magellan
`<aab_ende>` | Abschluss/Abbruch der Ausbildung kann rein logisch noch nicht erfolgt sein
`<sorgeberechtigter><as_einrichtung>` | Keine Entsprechung in Magellan