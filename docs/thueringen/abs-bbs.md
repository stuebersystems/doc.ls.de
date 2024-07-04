# Thüringen - ABS und BBS

Dieses Kapitel beschreibt für Berufsbildenden Schulen in Thüringen die benötigten Schritte zum Erstellen der elektronischen Landesstatistik für den Abgleich mit dem Kultusministerium in Thüringen im Schuljahr 2007/2008.



!!! info "Hinweis"

    Lesen Sie die Angaben und Vorgehensweise dieses Dokuments sehr genau und beachten Sie bitte alle Ihre Schulart betreffenden Aussagen.
Berufsbildende Schulen benötigen für die Landesstatistik jeweils das Stundenplanmodul von DaVinci zur Vervollständigung der Statistikdaten.

## Einführung

Die Statistik Thüringen wird seit dem Schuljahr 2007/2008 unterstützt. Grundlage des Statistikmoduls für Thüringen ist das Austauschformat, das in das Erfassungsprogramm des Kultusministeriums eingelesen wird.
Das Austauschformat ist eine mit Semikolon getrennte ASCII-Textdatei, die jeden Datensatz in einer Zeile hält. Diese Daten lassen sich z.B. nach dem Erstellen mit einem Texteditor betrachten.
Für Sie als Schule bedeutet dies: Sie müssen die folgende Textdatei erstellen und in das Erfassungsprogramm einlesen:

• SB_xxxxx.svs

Hierbei steht xxxxx für Ihre Schulnummer.
Die Datei erhält die Dateiendung .SVS, kann aber mit einem Texteditor problemlos eingelesen werden. 

Die Datei enthält einige Klassendaten, größtenteils aber Schülerdaten aus dem aktuellen Statistikjahr zum Stichtag.

Wie Sie diese Dateien an das Statistikamt versenden, wird Ihnen direkt durch das Statistikamt mitgeteilt.

## Notwendige Schritte

1. Schritt: [Statistikschlüssel bereinigen und aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Statistisch relevante Daten in DaVinci bzw. Magellan eingeben
3. Schritt: Kurswahlen von DaVinci nach Magellan übertragen (nur für Berufsbildende Gymnasien mit Oberstufe)
4. Schritt: Statistikdaten in das Magellan-Datawarehouse übertragen
5. Schritt: Statistikdaten im Magellan DWH-Explorer erstellen

## Eingaben in DaVinci

Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:

1. Öffnen Sie Magellan und wechseln Sie in die entsprechende Ansicht ``Schüler``, ``Klassen`` oder ``Lehrer``. Die Fächerliste finden Sie unter ``Verzeichnisse > Fächer``
2. Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
3. Öffnen Sie DaVinci und wechseln Sie in die entsprechende Ansicht der Stammdaten.
4. Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der DaVinci Ansicht und korrigieren Sie ggf. in DaVinci.

### Veranstaltungsliste

Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.

### Kurswahldaten und Lehrerdaten von DaVinci nach Magellan übertragen

Die Kurswahldaten (für Schulen mit Oberstufe) und die Lehrerdaten mit der Soll-Berechnung aus DaVinci (für die Sollberechnung) müssen für die Statistik nach Magellan übertragen werden. Nachdem Sie die Statistikkontrolle durchgeführt haben und die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten übernehmen, wie im DaVinci Handbuch im Kapitel „Spezielles“  unter „Datenaustausch mit Magellan“, „Daten nach Magellan übergeben“ beschrieben.

!!! info "Hinweis"

     Bitte beachten Sie, dass Sie nur mit Kopien der DaVinci Datei und Magellan Datenbank arbeiten!

## Übertrag ins Datawarehouse

So übertragen Sie Daten in das Datawarehouse:

1. Wählen Sie in Magellan die Ansicht ```Datawarehouse``` aus.
2. Klicken Sie dort unterhalb von ```Extras``` auf ```Starten```.
3. Der Importassistent für das Magellan-Datawarehouse wird gestartet.  Sie müssen sich jetzt erneut an der Magellan Datenbank mit der Administrator- Kennung und Kennwort anmelden.
4. Klicken Sie auf ```Weiter``` und wählen Sie den passenden Mandanten und  Zeitraum  aus.
5. Klicken Sie auf ```Weiter``` und dann auf ```Starten```. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

!!! info "Hinweis"

    Wenn Sie mit Halbjahren arbeiten, müssen Sie diesen Vorgang nur einmal ausführen, um die Daten aus dem aktuellen Zeitraum (1. Halbjahr) zu übertragen.

## Statistikdaten im Magellan-DWH-Explorer erstellen

Jetzt kann die Statistik mittels des Magellan DWH Explorer erstellt werden. Gehen Sie dabei wie folgt vor:

1. Klicken Sie auf ```Start```, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan 5/6 DWH Explorer.
2. Wählen Sie die Ansicht ```Auswertungen``` aus.
3. Wählen Sie unter Landesstatistik die Option ```Statistikformat für Thüringen``` aus und klicken Sie auf ```Starten```.
4. Folgen Sie nun den Anweisungen des Assistenten und klicken Sie auf ```Weiter```, um auf die nächste Karte zu kommen. 
5. Klicken Sie auf ```Weiter``` und folgen Sie den Anweisungen der nächsten Karte.
**Erhebungszeitraum**
Der „Erhebungszeitraum“ ist der Zeitraum in dem der Stichtag liegt. Dieser ist für die Statistik 2007 bei Verwendung von Halbjahren der 01.08.2007 bis zum 31.01.2008.
**Erstellungsdatum**
Tragen Sie das aktuelle Datum ein.
**Stichtag**
Tragen Sie den vom Kultusministerium festgelegten Stichtag für die Statistik ein.
**Exportordner**
Tragen Sie das Verzeichnis ein, in dem die fertigen Statistikdateien abgelegt werden sollen.
6. Klicken Sie auf ```Weiter``` und Sie erhalten eine letzte Übersicht der zu erstellenden Statistikdateien. Durch einen weiteren Klick auf ```Fertigstellen``` werden die Statistikdateien im Exportordner angelegt.

## Besonderheiten

### Bildungsgänge und Fachrichtungen

Die Schlüssel und Bezeichnungen für die Bildungsgänge und Fachrichtungen wurden miteinander kombiniert. Die Schlüssel werden im Statistikskript automatisch berechnet. Wenn keine Fachrichtung vorhanden war, wurde automatisch die Bezeichnung des Bildungsganges verwendet, ansonsten die Bezeichnung der Fachrichtung.

### Schüler und Klassendaten

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

**Statistikfeld** | **SJ > Schuljahr**
-|-
Datenfeld|-
Beschreibung|Das aktuelle Schuljahr wird automatisch eingetragen.
Statistikdatei |sa
Typ|P
**Statistikfeld** |**DAT > Eingabedatum**
Datenfeld |-
Beschreibung |Das aktuelle Datum wird automatisch eingetragen.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F1 > SNR (Schulnummer)**
Datenfeld |Magellan:Mandanten > Daten 1 > Schulnummer
Beschreibung |Tragen Sie im Feld „Schulnummer“ die Schulnummer Ihrer Schule ein.
Statistikdatei |sa
Typ|P
**Statistikfeld**|**F2 > Satzart(„Schüler“)**
Datenfeld|Magellan: Klassen > Daten > Schulart
Beschreibung|Tragen Sie im Feld „Schulart“ die Schulart der Klasse ein.<br> **Wichtig:** Von der korrekten Schulart hängt ab, ob z.B. die Kursfelder (bei Beruflichen Gymnasien) der Statistik gefüllt werden. Grundlage ist das Schlüsselverzeichnis ``Schularten``.
Statistikdatei|sa
Typ |P
**Statistikfeld**|**F3 > Schulteil**
Datenfeld |-
Beschreibung |Der Schulteil wird immer vorbesetzt und ist „1“.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F4 > lfd. Nr. der Klasse**
Datenfeld |Magellan:lassen > Daten > Statistikkürzel
Beschreibung|Tragen Sie im Feld „Statistikkürzel“ eine laufende Nummer für die Klassen ein, die für die Statistik berücksichtigt werden sollen.<br> **Wichtig:** Die laufende Nummer muss fortlaufend vergeben werden.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F5 > Y-Zug mit**
Datenfeld|Magellan:Klassen > Merkmale > Merkmal B1
Beschreibung|Tragen Sie im Feld „Merkmal B1“ die laufende Nummer der Klasse ein, mit der die aktuelle Klasse in mindestens einem Fach zusam-men unterrichtet wird.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F6 > Klassenbezeichnung**
Datenfeld|Magellan: Klassen > Daten > Kürzel
Beschreibung|Tragen Sie im Feld „Kürzel“ das Klassenkürzel der Klasse ein. Dieser wird bei der Statistik als Klassenbezeichnung verwendet.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F7 > Jahrgangsstufe**
Datenfeld |Magellan:Klassen > Zeiträume > Zeitraum > Jahrgang
Beschreibung |Tragen Sie im Feld „Jahrgang“ die Jahrgangsstufe der Klasse ein.<br> **Wichtig:** Erlaubt sind die Jahrgänge 1-4
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F8 > Unterrichtswochenstunden**
Datenfeld|DaVinci Stundenplan
Beschreibung|Die Unterrichtswochenstunden für die Schüler werden automatisch in DaVinci, anhand der gefüllten Veranstaltungsliste der Klasse berechnet.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F9 > lfd. Nr. des Schülers**
Datenfeld |-
Beschreibung|Wird automatisch vergeben und eingetragen.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F10 > Name**
Datenfeld |Magellan:Schüler > Daten 1 > Nachname
Beschreibung |Tragen Sie im Feld „Nachname“ den „Nachnamen“ des Schülers ein.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F11 > Vorname**
Datenfeld |Magellan:Schüler > Daten 1 > Vorname
Beschreibung|Tragen Sie im Feld „Vorname“ den „Vornamen“ des Schülers ein.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F12 > Geburtsdatum**
Datenfeld|Magellan:Schüler > Daten 1 > Geboren am
Beschreibung |Tragen Sie im Feld „Geboren am“ das „Geburtsdatum“ des Schülers ein.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F13 > Geschlecht**
Datenfeld |Magellan:Schüler > Daten 1 > Geschlecht
Beschreibung |Tragen Sie im Feld „Geschlecht“ das Geschlecht des Schülers ein.
Statistikdatei|sa
Typ |P
**Statistikfeld**|**F14 > Vorbildung**
Datenfeld|Magellan:Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss
Beschreibung |Tragen Sie im Feld „Abschluss“ die Vorbildung des Schülers ein. Grundlage ist das Schlüsselverzeichnis ``Abschlüsse (Extern)``.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F15 > Klassenart**
Datenfeld|Magellan: Klassen > Merkmale > Merkmal S2
Beschreibung|Tragen Sie im Feld „Merkmal S2“ die Klassenart ein. Grundlage ist das Schlüsselverzeichnis ``Schülermerkmale (Bereich S2)``.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F16 > Schulform**
Datenfeld|Magellan:Klassen > Daten > Schulform
Beschreibung |Tragen Sie im Feld „Schulform“ die Schulform der Klasse ein.Grundlage ist das Schlüsselverzeichnis ``Schulformen``.
Statistikdatei |sa
Typ|B
**Statistikfeld**|**F17 > nicht belegt**
Datenfeld |-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei |sa
Typ |B
**Statistikfeld** |**F18 > nicht belegt**
Datenfeld|-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei |sa
Typ |B
**Statistikfeld** |**F19 > Beruf/Bildungsgang**<br>**F69 > Fachrichtung**
Datenfeld |Magellan: Klassen > Daten > Bildungsgang
Beschreibung |Tragen Sie im Feld „Bildungsgang“ den Bildungs-gang/Fachrichtung der Klasse ein.Grundlage ist das Schlüsselver-zeichnis „Bildungsgaenge“.
Statistikdatei|sa
Typ|B
**Statistikfeld**|**F20 > Behinderte/Benachteiligte**
Datenfeld |Magellan:Schüler > Daten 4 > Behinderung
Beschreibung|Tragen Sie im Feld „Behinderung“ die Art der Behinderung ein. Grundlage ist das Schlüsselver-eichnis ``Behinderungsarten``.
Statistikdatei|sa
Typ|B
**Statistikfeld**|**F21 > nicht belegt**
Datenfeld|-
Beschreibung|Wird automatisch als Leerfeld eingetragen.
Statistikdatei|sa
Typ|B
**Statistikfeld**|**F22 > Zugang – Schulart**
Datenfeld |Magellan: Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulart<br>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung |Tragen Sie im Feld „Schulart“ die Schulart der zuvor besuchten Schule ein. Wählen Sie die Herkunftsschule im Feld ``Herkunftsschule`` aus. Grundlage ist das Schlüsselverzeichnis ``Schularten (Herkunft)``.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F23 > Zugang – Land**
Datenfeld |Magellan:Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen<br>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung |Tragen Sie im Feld „Unterlagen“ das Land der zuvor besuchten Schule ein. Wählen Sie die Herkunftsschule im Feld „Herkunftsschule“ aus.<br>Grundlage ist das Schlüsselverzeichnis ``Herkunftsunterlagen``.
Statistikdatei|sa
Typ |B
**Statistikfeld** | **F24 > nicht belegt**
Datenfeld|-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei|	sa
Typ|	B
**Statistikfeld**|**F25 > nicht belegt**
Datenfeld |-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei |sa
Typ|B
**Statistikfeld**|**F26 > nicht belegt**
Datenfeld |-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F27 > nicht belegt**
Datenfeld |-
Beschreibung|Wird automatisch als Leerfeld eingetragen.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F28 > Schulabschluss**
Datenfeld |Magellan: Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart
Beschreibung |Tragen Sie im Feld „Abschluss-art“ den Schulabschluss des Schülers ein. Grundlage ist das Schlüsselverzeichnis ``Abschlussarten``.
Statistikdatei|sa
Typ |B
**Statistikfeld** | **F29 > Entlassungsdatum**
Datenfeld |Magellan:S chüler > Zugang/Abgang > Abgang > AbgangAm
Beschreibung|Tragen Sie im Feld „Abgang am“ das Entlassungsdatum des Schülers ein.
Statistikdatei|sa
Typ |B
**Statistikfeld** | **F30 > Verlängerung**
Datenfeld | Magellan:Schüler > Laufbahn > Allgemein > Wiederholer
Beschreibung |Markieren Sie das Feld „Wiederholer“, wenn der Schüler das Schuljahr wiederholt.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F31 > Ausländer, Aussiedler**
Datenfeld|Magellan:Schüler > Statistik > Merkmal S1
Beschreibung|Tragen Sie im Feld „Merkmal S1“ den Aussiedler, bzw. Ausländer-status des Schülers ein.Grundlage ist das Schlüsselverzeichnis ``Schülermerkmale Bereich S1``.
Statistikdatei |sa
Typ |B
**Statistikfeld**| **F32 > Staatsangehörigkeit**
Datenfeld |Magellan:Schüler > Daten 2 > Staatsangehörigkeiten > Staatsangeh. 1
Beschreibung |Tragen Sie im Feld „Staatsangeh.1“ die Staatsangehörigkeit des Schülers ein. Grundlage ist das Schlüsselverzeichnis ``Staatsangehoerigkeiten``.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F33 > Wohnort**
Datenfeld|Magellan:Schüler > Daten 1 > Gemeinde
Beschreibung |Wählen Sie im Feld ``Gemeinde`` den entsprechenden Gemeindeschlüssel aus. Der Schlüssel für den Wohnort ergibt sich aus dem Gemeindeschlüssel.<br><br>Tipp:<br>Wenn Sie im Feld „PLZ“ eine bekannte Postleitzahl eintragen, wird der Gemeindeschlüssel automatisch für Sie eingetragen.<br>Grundlage ist das ``Postleitzahlenverzeichnis``.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F34 > Schülerstatus**
Datenfeld|Magellan:Schüler > Daten 2 > Umschulung > Umschulung
Beschreibung|Tragen Sie im Feld ``Umschulung``den Schülerstatus ein. Grundlage ist das Schlüsselverzeichnis ``Umschulungsmerkmale``.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F35 > Internat**
Datenfeld |Magellan:Schüler > Daten 4 > Betreuung > Einrichtung
Beschreibung |Tragen Sie im Feld „Einrichtung“ ein, ob es sich beim dem Schüler um einen Internatsschüler handelt.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F36 > Fahrtdauer**
Datenfeld|Magellan:Schüler > Daten 4 > Beförderung > Entfernung
Beschreibung |Tragen Sie im Feld „Fahrtdauer“ bei einem Internatsschüler die Fahrtdauer einer einfachen Fahrt zwischen Wohn- und Beschulungsort ein.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F37 > Religionszugehörigkeit**
Datenfeld |Magellan:Schüler > Daten 1 > Konfession
Beschreibung |Tragen Sie im Feld ``Konfession`` die Religionszugehörigkeit des Schülers ein.<br>Grundlage ist das Schlüsselverzeichnis ``Konfessionen``.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F38 > Religion – Abmeldung**<br> **F39 > Religion – Meldung**
Datenfeld|Magellan:Schüler > Daten 1 > Rel.-Wunsch
Beschreibung |Tragen Sie im Feld „Rel.-Wunsch„ die An- oder Abmeldung vom Religionsunterricht ein.<br>Grundlage ist das Schlüsselverzeichnis ``Religionswünsche``.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F40 > Religion/Ethik Teilnahme**
Datenfeld|Magellan:Schüler > Daten 1 > Rel.-Teilnahme
Beschreibung |Tragen Sie im Feld ``Rel.-Teilnahme`` die Teilnahme am Religionsunterricht ein.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F41 > Religionsunterrichtsort**
Datenfeld|Magellan:Schüler > Statistik > Merkmal T2
Beschreibung|Tragen Sie im Feld ``Merkmal T2`` die Schulnummer der Schule ein, wenn der Schüler nicht an der Stammschule Religionsunterricht erhält.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F42 > 1.FS-Status**<br> **F44 > 2.FS-Status**<br>**F46 > 3. FS-Status**
Datenfeld|Magellan:Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Tragen Sie im Feld ``Fachstatus`` für jede Fremdsprache den gültigen Fachstatus ein.<br><br>Mögliche Werte: „Pflicht“, „Wahlpf“ oder Freiw“<br><br>Berufliche Gymnasien: Bei Leistungskursen muss „1PF“ oder „2PF“ gesetzt werden, damit die Kurse für die Statistik korrekt erfasst werden.<br><br>Der Fremdsprachenstatus wird dann automatisch auf „Pflicht“ gesetzt.<br>Grundlage ist das Schlüsselverzeichnis ``Fachstati``.
Statistikdatei|sa
Typ |B
**Statistikfeld |F43 > 1.FS-Sprache**<br>**F45 > 2.FS-Sprache**<br>**F47 > 3. FS-Sprache**
Datenfeld |Magellan: Schüler > Daten 3 > Fremdsprachenfolge > 1. -3. Fremdsprache<br>Schüler > Zeugnis > Fächer > Fach
Beschreibung |Wählen Sie in den entsprechen-den Feldern die erteilten Fremdsprachen aus. Diese Fremdsprachen müssen auch als Fächer mit dem korrekten Fachstatus erfasst sein.<br>Grundlage ist das Schlüsselverzeichnis ``Fächer``.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F48 > nicht belegt**
Datenfeld |-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F49 > nicht belegt**
Datenfeld |-
Beschreibung |Wird automatisch als Leerfeld eingetragen.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F50 > 1. Leistungskurs**<br>**F51 > 2. Leistungskurs**
Datenfeld|Magellan: Schüler > Zeugnis > Fächer > FachSchüler > Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Nur Berufliche Gymnasien:<br>Wählen Sie im Feld „Fach“ den Leistungskurs aus. Wählen Sie im Feld „Unterrichtsart“ den Wert „LK “ für Leistungskurs aus.<br>Wählen Sie im Feld „Fachstatus“ je nach Gegebenheit einen der beiden Werte aus:<br><br>„1PF“ für 1. Prüfungsfach<br>„2PF“ für 2. Prüfungsfach
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F52 – F60 > 1. – 9. Grundkurs**<br>**F62 > 10. Grundkurs**
Datenfeld |Magellan: Schüler > Zeugnis > Fächer > Fach<br>Schüler > Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Nur Berufliche Gymnasien: Wählen Sie im Feld „Fach“ den Grundkurs aus. Wählen Sie im Feld „Unterrichtsart“ den Wert „GK “ für Grundkurs aus. Wählen Sie im Feld „Fachstatus“ den Fachstatus aus. Achten Sie auf die entsprechenden Werte für Fremdsprachen, siehe F43/F45/F47.
Statistikdatei |sa
Typ |B
**Statistikfeld**|**F61 > Seminarfach**
Datenfeld|Magellan: Schüler > Zeugnis > Fächer > FachSchüler > Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Nur Berufliche Gymnasien:<br>Wählen Sie im Feld „Fach“ das Seminarfach aus. Wählen Sie im Feld „Unterrichtsart“ den Wert „BL “ für Besondere Lernleistung aus. Wählen Sie im Feld „Fachstatus“ den Fachstatus aus.<br>Achten Sie auf die entsprechenden Werte für Fremdsprachen, siehe F43/F45/F47.
Statistikdatei |sa
Typ|B
**Statistikfeld**|**F63 > nicht belegt**
Datenfeld |-
Beschreibung|Wird automatisch als Leerfeld eingetragen.
Statistikdatei|sa
Typ |B
**Statistikfeld++|**F64-F66 > begonnen in der Jahrgangsstufe**
Datenfeld|Magellan:Schüler > Daten 3 > Fremdsprachenfolge > Von 
Beschreibung|Tragen Sie im Feld „Von“ jeweils den Beginn der Fremdsprache ein.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F67 > nicht belegt**
Datenfeld |-
Beschreibung|Wird automatisch als Leerfeld eingetragen.
Statistikdatei |sa
Typ|B
**Statistikfeld**| **F68 > Berufsfeld**
Datenfeld|Magellan:Klassen > Daten > Berufsfeld
Beschreibung |Tragen Sie im Feld “Berufsfeld” das Berufsfeld der Klasse ein. Grundlage ist das Schlüsselverzeichnis ``Berufsfelder``.
Statistikdatei|sa
Typ |B
**Statistikfeld**|**F70 > früherer Name**
Datenfeld|Magellan:Schüler > Statistik > Merkmal T2
Beschreibung |Tragen Sie im Feld ``Merkmal T2`` den früheren Namen des Schülers ein, falls der Name sich seit der letzten Statistik geändert hat.
Statistikdatei |sa
Typ|B
**Statistikfeld**|**F71 > Geburtsort-/land**
Datenfeld|Magellan:Schüler > Daten 1 > Geburtsort
Beschreibung|Tragen Sie im Feld „Geburtsort“ die langschriftliche Bezeichnung des Geburtsortes ein, wie er im Schlüsselverzeichnis ``Staatsangehoerigkeiten`` eingetragen ist.
Statistikdatei |sa
Typ |P
**Statistikfeld**|**F72 > Zugang – letzte Tätigkeit**
Datenfeld |Magellan:Schüler > Statistik > Merkmal S2
Beschreibung|Tragen Sie im Feld „Merkmal S2“ die letzte Tätigkeit ein. Grundlage ist das Schlüsselverzeichnis ``Schülermerkmale Bereich S2``.
Statistikdatei |sa
Typ|B
**Statistikfeld**|**F73 > Ort des Ausbildungsbetriebes**
Datenfeld|Magellan:Schüler > Ausbildung > Ausbildungsbetrieb
Beschreibung|Tragen Sie in der Liste der Ausbildungsbetriebe den Ausbildungsbetrieb des Schülers ein.<br>Für die Statistik wird automatisch die Gemeinde des Ausbildungsbetriebes ausgelesen. Voraussetzung ist, dass Sie einen Ausbildungsbetrieb bei den Betrieben mit Gemeindeschlüssel erfasst haben.
Statistikdatei|sa
Typ |B

