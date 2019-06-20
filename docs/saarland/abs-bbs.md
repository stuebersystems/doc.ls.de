# Saarland - ABS und BBS

Dieses Kapitel beschreibt für Allgemeinbildende und Berufsbildenden Schulen im Saarland die benötigten Schritte zum Erstellen der elektronischen Landesstatistik für den Abgleich mit dem Statistikamt im Schuljahr 2017/2018 und die Erzeugung der Eingabedaten für die Abiturstatistik (teilweise) und der Religionsstatistik.


!!! info "Hinweis"

    Lesen Sie die Angaben und Vorgehensweise dieses Dokuments sehr genau und beachten Sie bitte alle Ihre Schulart betreffenden Aussagen.
    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

## Einführung

Das statistische Landesamt fordert die elektronische Landesstatistik im CSV Dateiformat. Die statistischen Daten können in diesem Format aus Magellan heraus erzeugt werden.
Für Sie als Schule bedeutet dies: Sie müssen die folgenden CSV-Dateien an das Statistikamt im Saarland verschicken (Schulbogen und Klassenbogen) und auf Basis der erzuegten CSV-Dateien für die Abiturstatistik und Religionsstatistik die entsprechenden Statistikbögen ausfüllen.

| Statistiktyp       | Dateiname   | Inhalt
| :---               | :---        | :---
| Klassenbogen       | KA01.csv    |Schüler/-innen insgesamt
| Klassenbogen       | KA02.csv    |Schüler/-innen nach Religionszugehörigkeit
| Klassenbogen       | KA03.csv    |Schüler/-innen nach Geburtsjahrgängen
| Klassenbogen       | KA04.csv    |Ausländische Schüler/-innen nach Geburtsjahrgängen
| Klassenbogen       | KA05.csv    |Schulische Herkunft der Schüler/-innen
| Klassenbogen       | KA06.csv    |Ausländische Schüler/-innen nach Staatsangehörigkeit
| Klassenbogen       | KA07.csv    |Teilnehmer/-innen am pflichtmäßigen Fremdsprachenunterricht 
| Klassenbogen       | KA08.csv    |Teilnehmer/-innen am freiwilligen Fremdsprachenunterricht 
| Klassenbogen       | KA09.csv    |Kurse nach Frequenzgruppen (nur auf Klassenstufen 11-13)
| Klassenbogen       | KA10.csv    |Schüler/innen nach Unterrichtsfächern und Art der Kurse (nur Klassenstufen 11-13)
| Klassenbogen       | KA12.csv    |Wiederholer/innen der Klassenstufe nach Schularten
| Klassenbogen       | KA13.csv    |Regionale Herkunft der Schüler/innen
| Klassenbogen       | KA15.csv    |Schüler/innen, die im Laufe des abgelaufenen Schuljahres  freiwillig aus der nächsthöheren in diese Klasse zurückgetreten sind
| Klassenbogen       | KA16.csv     |Bei überwiegender nichtdeutscher Verkehrssprache in der Familie: Sprache bzw. Sprachengruppe
| Schulbogen         | TAB_1_1.csv  |Schüler in den Klassenstufen (Teil 1)
| Schulbogen         | TAB_1_2.csv  |Schüler in den Klassenstufen (Teil 2)
| Schulbogen         | TAB_2_A.csv  |Schulabgänger/-innen nach Beendigung der Vollzeitschulpflicht zum Ende des abgelaufenen Schuljahres nach Abschlussarten und Klassenstufen
| Schulbogen         | TAB_2_B.csv  |Schulabgänger/-innen nach Beendigung der Vollzeitschulpflicht zum Ende des abgelaufenen Schuljahres nach Abschlussarten und Alter
| Schulbogen         | TAB_3.csv    |Ausländische Schulabgänger/-innen nach Beendigung der Vollzeitschulpflicht zum Ende des abgelaufenen Schuljahres nach Staatsangehörigkeit und Abschlussarten
| Schulbogen         | TAB_4_12.csv |Tabellen 4, 5, 6, 7, 11 und 12 des Schulbogens  
| Abiturstatistik    | Abitur_Anlage2.csv       | Auswertung der schriftlichen Abiturprüfung pro Fach und Berechnung des Durchschnittgeburtsdatums
| Abiturstatistik    | Abitur_Anlage3.csv       | Auswertung Abiturdurchschnittsnoten
| Religionsstatistik | Religion_Schueler.csv    | Religionsunterricht nach Klassenstufen und Schülern
| Religionsstatistik | Religion_Lerngruppen.csv | Religionsunterricht nach Lerngruppen
| Religionsstatistik | Religion_Lehrer.csv      | Religionsunterricht nach Lehrern

## Notwendige Schritte

1. Schritt: Statistikschlüssel aktualisieren
2. Schritt: Statistisch relevante Daten in MAGELLAN eingeben
3. Schritt: Statistikdaten erstellen.

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

|Nr.|So geht's|
|--|--|
|1.| Stellen Sie sicher, dass Sie die aktuellste Ausgabe von MAGELLAN 6 einsetzen!|
|2.| Öffnen Sie das Modul MAGELLAN- Administrator und wählen die Ansicht `Datenimporte > Schlüsselverzeichnisse` importieren.|
|3.| Wählen Sie `Saarland`, Ihrer Schulart und Ihren Mandanten aus und importieren einen ausgewählten oder alle mitgelieferten Kataloge.|


!!! warning "Wichtig"

    Sie haben bereits Schlüsselzeilen in Ihrer Datenbank verwendet, für die Sie eigene Werte in der Spalte `Schlüssel` eingetragen haben.
    Durch diese eigenen Werte haben wir nicht die Möglichkeit beim Import der neuen Schlüssel diese mit Ihren Schlüsseln abzugleichen.
    Es muss mindestens beim ersten Statistikdurchlauf (ab dem nächsten Jahr können dann Schlüssel erkannt werden) ein manuelle Nacharbeit erfolgen. Bitte lesen Sie dazu den nächsten Abschnitt!

### Manuelle Anpassung der Schlüsselverzeichnisse in MAGELLAN 6

Beim Import der Schlüssel gibt es einen Ablauf, der gewähren soll, dass die Wahrscheinlichkeit einen inaktuellen oder verkehrten Schlüssel im Alltag zu verwenden, minimiert wird. 

### Einleseprozess

|Nr.|Was passiert beim Einlesen?|
|--|--|
|1.|Alle noch nie verwendeten Schlüsselzeilen werden gelöscht.<br/>Übrig bleiben nur die Zeilen, die Sie bereits einmal verwendet haben.<br/>Diese Zeilen können jetzt für die Statistik richtig oder auch verkehrt sein.
|2.|Alle übrigen Zeilen werden mit einer grauen Raute als inaktive Schlüssel gekennzeichnet.<br/><br/> Zur Erklärung: Jedes Verzeichnis hat die Spalten `von` und `bis`. In diesen Spalten kann man ein Datum eintragen, das wird bei der Anzeige mit dem ausgewählten Zeitraum in MAGELLAN verglichen und der Schlüssel wird demnach mit einer grauen oder einer blauen Raute in der Programmoberfläche gezeigt. Schlüssel mit einer grauen Raute werden zusätzlich ans Ende der Liste sortiert.
|3.|Als nächstes wird ein Schlüssel aus dem Importkatalog anhand seines Schlüsselwerts (Inhalt der Spalte `Schlüssel`) mit den im Verzeichnis noch enthaltenen Schlüsseln verglichen. Werden Zeilen erkannt (gleicher Schlüsselwert), wird der Schlüssel (oder werden die Schlüssel, es dürfen auch mehrere Zeilen existieren) wieder aktiviert, das heißt der oder die Schlüsselzeilen werden als aktive Schlüssel mit einer blauen Raute dargestellt.<br/>Ist keine Zeile mit dem verglichenen Schlüssel im Verzeichnis vorhanden, wird die Schlüsselzeile im Verzeichnis mit angelegt - ist aber bislang nirgendwo im Programm mit einem Datensatz verbunden.|

### Ihre Schlüsselwerte an Vorgaben des Ministeriums anpassen

Um Ihre verwendeten Schlüsseldatensätze auf die Vorgaben des Ministeriums anzupassen, ist noch manuelle Nachpflege erforderlich:

|Nr.|So geht's|
|--|--|
|1.|Nach dem Einlesen öffnen Sie bitte jedes relevante Verzeichnis (Liste der relevanten Schlüsselverzeichnisse nachstehend).|
|2.|Sortieren die Schlüssel nach dem `Bis`-Datum, so das Zeilen mit einem `Bis`-Datum oben angeordnet sind. |
|3.|Sind Schlüssel mit einem Eintrag vorhanden? <br/>Dann müssen diese Datensätze jetzt noch editiert werden. <br/>Es handelt sich vermutlich um Werte, die Sie in der Datenbank bereits verwendet haben, die aber nicht den korrekten Schlüsselwert haben. <br/><br/>**Bitte löschen Sie nicht diese Schlüssel!**|
|4.|Wenn Ihr Schlüssel nicht erkannt wurde und daher als inaktiv erkannt wurde, dann hat der Einleseprozess in der Liste, die Sie gerade geöffnet haben, auch den korrekten Schlüssel ergänzt. <br/>Bitte schauen Sie nach, kopieren den Wert aus dem Feld `Schlüssel` und geben Sie diesen Wert für Ihren Schlüssel im Feld `Schlüssel` ein.|
|5.| Entfernen Sie anschließend das `Bis`-Datum für diese Zeile und gehen für die weiteren Zeilen genauso vor.|
|6.|Wenn Sie die SAXSVS-relevanten Verzeichnisse geprüft und entsprechend angepasst haben, lesen Sie bitte die Schlüssel erneut ein! <br/><br/> Überzählige Schlüsseldatensätze werden dann wieder entfernt und Sie erhalten bei eventuell übersehenden Zeilen erneut ein `Bis`-Datum als Zeichen, das hier noch etwas korrigiert werden müsste.<br/> Ist nach dem Einlesen keine `Bis`-Datum mehr gefüllt, sind Ihre Schlüsselwerte korrekt und auch Ihren Schülern zugeordnet. <br/>Mit dieser Schlüsselbasis können dann auch im nächsten Jahr die Schlüssel einfach nur importiert werden, die manuelle Nacharbeit entfällt. 

### Welche Importdateien stehen zur Verfügung?

Importdatei|Zielverzeichnis in MAGELLAN
--|--
BS_Berufe.keys|`Verzeichnisse > Berufe`
00_AbschluesseIntern.keys|`Verzeichnisse > Abschlüsse (Intern)`
00_Fachstati.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Fachstatus`
00_Faecher.keys|`Verzeichnisse > Fächer`
00_Konfessionen.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Konfessionen`
00_Muttersprachen.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Muttersprachen`
00_Noten.keys|`Verzeichnisse > Noten`
00_RelTeilnahmen.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Religion (Teilnahmen)`
00_Schulformen.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Schulformen`
00_SchulformenHerkunft.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Schulformen (Herkunft)`
00_Sprachreferenzen.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Sprachreferenzen`
00_Staatsangehoerigkeiten.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Staatsangehörigkeiten`
00_Unterrichtsarten.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Unterrichtsarten`
00_Versetzungsarten.keys|`Verzeichnisse > Weitere Schlüsselverzeichnisse > Versetzungsarten`

## Statistisch relevante Daten in MAGELLAN eingeben

In den nachfolgenden Abschnitten wird pro Statistiktyp beschrieben, welche Daten in MAGELLAN wichtig sind, damit die entsprechenden CSV-Dateien gefüllt werden können.

!!! warning "Wichtig"

    Einige Eintragungen werden wiederholt erwähnt, da sie für mehrere Auswertungen Voraussetzungen sind.


### Klassenbogen

Datenfeld in MAGELLAN                           |Beschreibung  MAGELLAN:
------------------------------------------------|-------------------------------------------------------
Klassen > Daten > **Statistikkürzel** |Es werden alle Schüler berücksichtigt, bei deren Klasse ein Statistikkürzel eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein. 
Klassen > Zeiträume > **Fachtafel** |Der Klasse muss im aktuellen Zeitraum der Statistikerhebung eine Fachtafel zugeordnet sein. Dies ist nur für Fachtafeln der Klassenstufen 11-13 notwendig. Legen Sie die entsprechenden Fachtafeln unter `Verzeichnisse > Fachtafeln` an und weisen sie unter `Klassen > Zeiträume > Fachtafel` zu.
Klassen > Zeiträume > **Jahrgang** |Geben Sie hier den Jahrgang der Klasse an.
Verzeichnisse > Fachtafeln > Details > **Fach**, **Unterrichtsart**, **KursNr**, **Lehrer**, **Ist-Stunden**|Hier ist die Fachtafel der Klasse definiert. Hier müssen alle Kurse der Klasse, definiert durch Fach + Unterrichtsart + KursNr definiert werden mit zugehörigem Lehrer und der Ist-Stundenzahl. Die Ist-Stunden und Lehrer-Angabe ist nur für Klassen der Klassenstufen 11-13 notwendig.
Schüler >  Zeugnis > Fächer > **Fach**, **Unterrichtsart**, **Fachstatus**, **KursNr**, **Lehrer** | Jeder Schüler:<br/>Pro Schüler wird hier hier im aktuellen Erhebungszeitraum die Zugehörigkeit zu einer Lerngruppe aus Fach + Unterrichtsart + KursNr und dem unterrichtenden Lehrer definiert. <br/>Nur Oberstufe:<br/>Das Feld `Fachstatus` ist nur bei Fremdsprachen zu füllen, wenn die Fremdsprache freiwillig ist. Dies ist nur für Schüler der Klassenstufen 11-13 notwendig.
Schüler >  Daten 1 > **Geschlecht**, **Geboren am**, **Konfession**, **Gemeinde**, **Stadtbezirk**| Pro Schüler wird das Geschlecht, die Konfession und das Geburtsdatum eingetragen. Zusätzliche muss die Gemeindekennziffer im Feld `Gemeinde` und der zugehörige Gemeindeteil unter `Stadtbezirk` eingetragen werden.
Schüler >  Daten 2 > **Staatsangehörigkeit 1**, **Verkehrssprache**| Pro Schüler wird die `Staatsangehörigkeit` und bei Bedarf die `Verkehrssprache` eingetragen.
Schüler >  Daten 3 > **Fremdsprache 1-3**| Pro Schüler sind hier die `Fremdsprachen` einzutragen. Hierfür können Sie auch die Sammelzuweisung unter `Schüler > Bearbeiten  > Sammelzuweisung` nutzen.
Schüler > Laufbahn > Allgemein > **Versetzungsart** |Hier ist für Schüler des vorherigen Schuljahres anzugeben, ob diese freiwillig zurückgetreten sind.<br/>Hierfür können Sie auch die Sammelzuweisung unter `Schüler > Bearbeiten  > Sammelzuweisung` nutzen.
Schüler > Zugang/Abgang > **Voraus. Ende**|Hier ist das Feld auszufüllen, wenn der Schüler innerhalb des aktuellen Schuljahres voraussichtlichen entlassen wird.
Schüler > Laufbahn > Allgemein > **Wiederholer**| Geben Sie hier im aktuellen Erfassungzeitraum an, ob der Schüler ein Wiederholer ist
Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunft > **Schulform**. | Geben Sie hier die `Schulform` der Schule an, von der der Schüler gekommen ist. 

### Schulbogen

Voraussetzung für die Auswertungsteile für das Abitur ist, dass die auszuwertenden Schüler im aktuellen Erhebungszeitraum in der Ansicht `Abitur` vorhanden sind.

Datenfeld in MAGELLAN                           |Beschreibung  MAGELLAN:
------------------------------------------------|-------------------------------------------------------
Klassen > Daten > **Statistikkürzel** |Es werden alle Schüler berücksichtigt, bei deren Klasse ein `Statistikkürzel` eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein.
Klassen > Zeiträume > **Jahrgang** |Geben Sie hier den `Jahrgang` der Klasse an.
Schüler >  Daten 1 > **Geschlecht**, **Geboren am**, **Konfession**| Pro Schüler wird das `Geschlecht`, das `Geburtsdatum` und die `Konfession` eingetragen. 
Schüler >  Laufbahn > Abschluss > **Abschluss 1**| Im vorherigen Schuljahr sind hier die evtl. Abschlüsse der Schüler einzutragen
Schüler >  Daten 2 > **Staatsangehörigkeit 1**| Pro Schüler wird hier die `Staatsangehörigkeit` eingetragen.
Abitur > Qualifikation > **Status**, **Abitur angemeldet**|Pro Schüler kann unter `Status` ausgewiesen, dass er die ``Zulassung 12 erreicht`` bzw. das Abitur bestanden hat. Zusätzlich kann ausgewählt werden, ob er sich zum Abitur angemeldet hat.
Abitur > Prüfung > **Prüfungsstatus** | Geben Sie hier den `Prüfungsstatus` an.

### Religionsstatistik

Datenfeld in MAGELLAN                           |Beschreibung  MAGELLAN:
------------------------------------------------|-------------------------------------------------------
Klassen > Daten > **Statistikkürzel** |Es werden alle Schüler berücksichtigt, bei deren Klasse ein `Statistikkürzel` eingetragen wurde. Das `Statistikkürzel` sollte gleich dem Klassenkürzel sein. 
Klassen > Zeiträume > **Fachtafel** |Der Klasse muss im aktuellen Zeitraum der Statistikerhebung eine `Fachtafel` zugeordnet sein. 
Verzeichnisse > Fachtafeln > Details > **Fach**, **Unterrichtsart**, **KursNr**, **Lehrer**, **Ist-Stunden**|Hier ist die `Fachtafel` der Klasse definiert. Hier müssen alle Kurse der Klasse, definiert durch Fach + Unterrichstart + KursNr definiert werden mit zugehörigem Lehrer und der Ist-Stundenzahl. Dabei muss das Fach der katholische Religionsunterricht, der evangelische Religionsunterricht oder Ethik sein.
Schüler >  Daten 1 > **Konfession**, **Rel.-Teilnahme**| Pro Schüler wird die Konfession und die Religionsteilnahme eingetragen.
Schüler >  Zeugnis > Fächer > **Fach**, **Unterrichtsart**, **KursNr**, **Lehrer** | Pro Schüler wird hier im aktuellen Erhebungszeitraum die Zugehörigkeit zu einer Lerngruppe aus Fach + Unterrichtsart + KursNr und dem unterrichtenden Lehrer definiert. Dabei muss das Fach der katholische Religionsunterricht, der evangelische Religionsunterricht oder Ethik sein.  
Lehrer > Daten > **Vorname**, **Nachname**|Hier muss jeder Lehrer definiert werden, der in den Fächern der Schüler bzw. der Fachtafel der Klasse dem Religions- bzw. Ethikunterricht zugeordent ist.

### Abiturstatistik

Voraussetzung für die Abiturstatistik ist, dass die auszuwertenden Schüler im aktuellen Erhebungszeitraum in der Ansicht `Abitur` vorhanden sind.

Datenfeld in MAGELLAN                           |Beschreibung  MAGELLAN:
------------------------------------------------|-------------------------------------------------------
Schüler >  Daten 1 > **Geschlecht**, **Geboren am**| Pro Schüler wird hier das Geschlecht und das Geburtsdatum angegeben
Abitur > Prüfung > **Prüfungsfach 1-4** | Hier müssen die Prüfungsfächer 1- 4 angeben werden, in den die schriftliche Prüfung erfolgt
Abitur > Prüfung > **Schriftl. Noten in Prüfungsfach 1-4** | Hier müssen die Prüfungsfächer 1-4 die evtl. schriftlichen Prüfungsnoten angeben werden
Abitur > Prüfung > **Durchschnitt** | Hier muss die Abiturnote eingetragen werden.

## Statistikdaten erstellen

Zum Erstellen der Statistikdateien gehen Sie wie folgt vor:

1. Starten Sie MAGELLAN.
2. Klicken Sie im Menü `Extras` auf `Statistik`.
3. Wählen Sie als Bundesland ``Saarland``. Klicken Sie dann auf `Weiter`.
4. Markieren Sie die Dateien, welche Sie erstellen möchten. Unter Statistikzeiträume auswählen müssen Sie den Erhebungszeitpunkt (Beispiel 02.11.2018), den aktuellen Zeitraum (1. Halbjahr 2018/2019) und die Zeiträume des Vorjahres (2. Halbjahr 2017/2018 und 1. Halbjahr 2017/2018) einstellen.
5. Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf `Weiter`. Klicken Sie auf `Start`, um die Erstellung der Statistikdateien zu starten.