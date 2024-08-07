# Niedersachsen - ABS

## Lizenz und Version

Für das Erzeugen der Schnittstellendatei wird die jährliche Lizenz für das Modul "Modul LANDESSTATISTIK Niedersachsen ABS" benötigt. Damit können die Daten für die amtliche Statistik Niedersachsen (IZN-Stabil) erzeugt werden. Zusätzlich ist Support zum Modul und das jeweilige Jahr enthalten.

## Grundsätzliches

Mit DaVinci und Magellan können Sie die Datensätze erstellen, die für die Erhebung der amtlichen Landesschulstatistik für allgemeinbildendende Schulen in Niedersachsen benötigt werden. Wenn Sie nur Magellan besitzen, können Sie nur die Klassendatei für den Import nach izn-Stabil erzeugen.

!!! info "Hinweis"

   Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Mit Magellan bzw. Magellan und DaVinci können die folgenden Dateien erzeugt werden:

Datei |Beschreibung |Voraussetzung
--|--|--
KLIMP.TXT |Aktuelle Klassen- und Schülerdaten |Magellan-Lizenz
LVIMP.TXT |Aktuelle Lehrerdaten |Magellan- und DaVinci-Lizenz
RELIMP.TXT |Aktuelle Daten zum Religionsunterricht bzw. Unterricht Werte und Normen |Magellan- und DaVinci-Lizenz

Die erzeugten Dateien können dann in das Statistikprogramm izn-Stabil importiert werden. Die Oberstufendatei SEK2IMP.TXT wird noch nicht unterstützt. Voraussetzung für die Nutzung der Statistikschnittstelle ist eine Lizenz von Magellan bzw. Magellan und DaVinci. 

## Notwendige Schritte

1. Schritt: [Statistikschlüssel aktualisieren](https://doc.ls.stueber.de/schluesselverzeichnisse/) 
2. Schritt: Dateneingabe
3. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
4. Schritt: Statistikdateien erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](https://doc.ls.stueber.de/schluesselverzeichnisse/).

## Statistikrelevante Daten eingeben

Bei einem Großteil der statistikrelevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang in einer tabellarischen Übersicht.
Statistikrelevante Daten in Magellan überprüfen 
Bevor Sie die Statistikdateien erstellen können, sollten Sie unbedingt prüfen, ob Sie alle statistikrelevanten Daten korrekt eingegeben haben. Hierzu stellen wir Ihnen einige Hilfen zur Verfügung.

Mit Hilfe der automatischen Statistikkontrolle können Sie viele der eingegebenen Daten prüfen. Pflichtfelder werden auf Vorhandensein und teilweise auf syntaktische Korrektheit geprüft (z.B. Anzahl der Stellen bei zweistelligen Schlüsseln). Anhand der Rückmeldungen müssen Sie die Daten korrigieren.
So starten Sie die automatische Statistikkontrolle in Magellan:

1. Wechseln Sie in das jeweils zu prüfende Halbjahr.
2. Klicken Sie im Menü Extras auf ```Statistikkontrolle```
3. Wählen Sie im Feld Bundesland, Niedersachsen ABS aus.
4. Wählen Sie im Feld Kontext aus, welche Daten geprüft werden sollen. Wählen Sie Schüler ABS um die Schüler- und Klassendaten des aktuellen Zeitraums zu prüfen.
5. Es erscheint das Fenster mit den Prüfungsmeldungen, die Sie in die Zwischenablage kopieren können, um Sie dann z.B. über Word auszudrucken.
6. Gehen Sie bitte alle Warnungen und Hinweise sorgfältig durch und korrigieren Sie ggf. Fehler in den Eingaben.

## Statistikdaten in das Magellan-Datawarehouse übertragen

So übertragen Sie Magellan-Daten in das Datawarehouse:

1. Wählen Sie in Magellan die Ansicht Datawarehouse aus.
2. Klicken Sie dort unterhalb von Extras auf Starten.
3. Der Importassistent für das Magellan-Datawarehouse wird gestartet. Sie müssen sich jetzt erneut an der Magellan Datenbank mit der Administrator- Kennung und Kennwort anmelden.
4. Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und Zeitraum aus. Für die Erhebung im Februar wäre dies der Zeitraum des 2. Halbjahres des neuen Schuljahres.
5. Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

So archivieren Sie DaVinci-Daten ins Datawarehouse:

1. Starten Sie DaVinci-Stundenplan mit Ihrer Plandatei.
2. Wählen Sie Extras und dann Archivieren aus.
3. Bestätigen Sie die Sicherheitsabfrage. Die Daten werden jetzt in eine Schuldatentransferdatei exportiert, anschließend wird der Importassistent für das Magellan-Datawarehouse gestartet. Sie müssen sich jetzt in Magellan mit der Administrator- Kennung und Kennwort anmelden.
4. Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und Zeitraum aus.
5. Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

Nutzen Sie nur Magellan für die Statistik, so entfällt der Schritt der Archivierung der DaVinci-Daten ins Datawarehouse.

!!! info "Hinweis"

    Übertragen Sie immer zuerst die Daten aus Magellan und dann aus DaVinci in das Datawarehouse.

## Statistikkontrolle im Magellan-DWH-Explorer durchführen

Wenn alle Daten in das Datawarehouse übertragen wurden, können Sie mit Hilfe des Magellan DWH Explorer sich den Inhalt des Magellan-Datawarehouse anzeigen lassen. 

Gehen Sie dabei wie folgt vor:

1. Klicken Sie auf Start, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan DWH Explorer.
2. Wählen Sie die Ansicht Datenbestand aus.
3. Wählen Sie den passenden Mandanten aus und tragen Sie einen passenden Zeitpunkt ein. Möchten Sie die aktuellen Schuldaten betrachten, beispielsweise das heutige Datum. Sie können nun durch Wechseln der Registerkarten die eingetragenen Klassen, Schüler, Lehrer usw. betrachten.

## Statistikdaten für den Import nach izn-Stabil erstellen

Jetzt können die Statistikdaten mittels des Magellan DWH Explorer erstellt werden. Gehen Sie dabei wie folgt vor:

1. Starten Sie den Magellan DWH Explorer über den Punkt Programme |STÜBER SYSTEMS| Magellan DWH Explorer.
2. Wählen Ansicht und dann Statistiken.
3. Wählen Sie unter Landesstatistik die Option Statistik für Niedersachsen (ABS) aus.
4. Wählen Sie im Dialogfenster Exportiere nach izn-Stabil einen Exportordner für die zu exportierenden Dateien, einen Mandanten und geben Sie den Zeitraum der Statistikerhebung ein. Klicken Sie dann auf OK.
5. Die Daten werden jetzt in die Dateien LVIMP.TXT, KLIMP.TXT und RELIMP.TXT in den zuvor angegebenen Ordner exportiert.

Wie Sie diese Dateien nach izn-Stabil importieren können, entnehmen Sie bitte der Dokumentation zu izn-Stabil bzw. der Online-Hilfe zu izn-Stabil.

Wenn Sie nur eine Lizenz von Magellan besitzen, dürfen Sie nur die Datei KLIMP.TXT nach izn-Stabil importieren.

## Besonderheiten

### 2016/2017

#### Verzeichnis Staatsangehörigkeiten

Schlüssel Alt |Schlüssel Neu|Bezeichnung |Änderung
--|--|--|--
133 |170|Serbien|Schlüssel

### Allgemeine Daten

!!! info "Hinweis"

      Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Datenfeld in Magellan/DaVinci  |Beschreibung |Statistikdatei| Typ
--|--|--|--
Magellan:Mandanten > Daten 1 > Schulnummer| Geben Sie hier Ihre 5-stellige Schulnummer ein. |Alle Statistikdateien| P

### Schüler- und Klassendaten

!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Datenfeld in    Magellan/DaVinci|Beschreibung|Statistikdatei|Typ
--|--|--|--
Magellan:     Klassen > Daten > Statistikkürzel|Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie unter Statistikkürzel nichts eintragen.|KLIMP.TXT|P
Magellan:     Klassen > Daten > Schulform|Geben Sie hier die Schulform ein. Grundlage ist das Schlüsselverzeichnis „Schulformen“.|KLIMP.TXT|P
Magellan:    Klassen > Merkmale > Merkmal S1|Geben Sie hier an, ob die Klasse eine Integrationsklasse ist. Grundlage ist das Schlüsselverzeichnis „Klassenmerkmale“ (Bereich S1). Keine Angabe entspricht dem Wert „Nein“.|KLIMP.TXT|P
Magellan:    Klassen > Merkmale > Merkmal S2|Geben Sie hier an, ob die Klasse eine Sprachlernklasse ist. Grundlage ist das Schlüsselverzeichnis „Klassenmerkmale“ (Bereich S2). Keine Angabe entspricht dem Wert „Nein“.|KLIMP.TXT|P
Magellan:    Klassen > Merkmale > Merkmal S3|Geben Sie hier an, ob die Klasse eine Eingangsstufe ist. Grundlage ist das Schlüsselverzeichnis „Klassenmerkmale“ (Bereich S3). Keine Angabe entspricht dem Wert „Nein“.          Nur für Grundschulen Pflichtfeld!|KLIMP.TXT|B
Magellan:  Klassen > Zeiträume > Zeitraum >     Jahrgang|Geben Sie hier den Jahrgang der Klasse ein.     |KLIMP.TXT|P
Magellan:    Schüler > Daten 1 > Geschlecht|Geben Sie hier das Geschlecht ein.|KLIMP.TXT|P
Magellan:          Schüler > Daten 1 > Geboren am|Geben Sie hier das Geburtsdatum ein.|KLIMP.TXT|P
Magellan:     Schüler > Daten 1 > Konfession|Geben Sie hier die Religionszugehörigkeit der Schüler an. Grundlage ist das Schlüsselverzeichnis „Konfessionen“.|KLIMP.TXT|P
Magellan:  Schüler > Daten 1 > Rel.-Teilnahme|Geben Sie hier die Religionsteilnahme der Schüler an. Grundlage ist das Schlüsselverzeichnis „Religion (Teilnahmen)“.|KLIMP.TXT|P
Magellan: Schüler > Daten 2 > Staatsangeh. 1|Geben Sie hier die Staatangehörigkeit der Schüler mit ausländischer Herkunft an. Grundlage ist das Schlüsselverzeichnis „Staatsangehörigkeiten“.|KLIMP.TXT|P
Magellan: Schüler > Daten 2 > Muttersprache|Geben Sie hier für Schüler nichtdeutscher Herkunftssprache die Muttersprache ein. Grundlage ist das Schlüsselverzeichnis „Muttersprachen“|KLIMP.TXT|P
Magellan: Schüler > Daten 4 > Förderung|Geben Sie hier an, ob Schüler nichtdeutscher Herkunftssprache einen Förderbedarf in Deutsch besitzen. Grundlage ist das Schlüsselverzeichnis „Förderungen“|KLIMP.TXT|P
Magellan:Schüler > Statistik > Merkmal S1|Geben Sie hier die Herkunft der Schüler an. Grundlage ist das Schlüsselverzeichnis „Schülermerkmale“ (Bereich S1).|KLIMP.TXT|P
Magellan: Schüler > Statistik > Merkmal S2|Geben Sie hier die Herkunft der Schüler an. Grundlage ist das Schlüsselverzeichnis „Schülermerkmale“ (Bereich S2).|KLIMP.TXT|P
Magellan:Schüler > Laufbahn > Allgemein >  Wiederholer|Je nachdem, ob es sich um einen Wiederholer handelt oder nicht, haken Sie das Feld „Wiederholer“ oder „Überspringer“ an.            Nur für Jahrgang 5 Pflichtfeld!|KLIMP.TXT|B
Magellan:    Schüler > Zugang/Abgang >  Bereits besuchte Schulen |Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.    Das Feld „Schulart“ muss angegeben werden, damit die Schülerzahlen pro Herkunftsschulart berechnet werden kann. Beachten Sie bitte, dass im Feld „Herkunftsart“ die Laufbahnempfehlung eingetragen sein muss. Grundlage ist das Schlüsselverzeichnis „Schularten (Herkunft)“. Das Feld „Zugang am“ muss gefüllt sein, damit der Schüler als Neuzugang erkannt wird. Nur für Jahrgang 5 Pflichtfeld!  Im Feld „Abgangsart“ wird zur Berechnung der Schülerzahlen pro Schulart, die nachfolgende Schulart angegeben.      Grundlage ist das Schlüsselverzeichnis „Abgangsarten“.|KLIMP.TXT|B  
|Magellan: Schüler > Zugang/Abgang >  Bereits besuchte Schulen > Herkunftsart  ||   
|Magellan:Schüler > Zugang/Abgang >     Herkunftsschule     ||
|Magellan:Schüler > Zugang/Abgang >    Zugang am  >    Schüler > Zugang/Abgang > Abgangsart||
Magellan: Schüler > Zeugnis > Fächer > Fach|Geben Sie hier pro Schüler die unterrichteten Fremdsprachen an. Zusätzlich sind hier die Fächer für Philosophie, evangelischen, katholischen, islamischen, konfessionell-kooperativen Religionsunterricht bzw. Unterricht Werte und Normen einzutragen, sofern diese vom Schüler belegt werden. Grundlage ist das Schlüsselverzeichnis „Fächer“.|KLIMP.TXT /RELIMP.TXT|B
DaVinci-Stundenplan Veranstaltungsliste|Die Anzahl der Lerngruppen und deren jeweilige Stunden für die Fächer Philosophie, evangelischen, katholischen, islamischen, konfessionell-kooperativen Religionsunterricht bzw. Unterricht Werte und Normen ergibt sich aus der Veranstaltungsliste in DaVinci.|RELIMP.TXT|B

## Lehrerdaten
#
!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Datenfeld in   Magellan/DaVinci|Beschreibung|Statistikdatei|Typ
--|--|--|--
Magellan:  Lehrer > Daten 1 > Nachname|Geben Sie hier den Nachnamen ein.|LVIMP.TXT|P
Magellan:  Lehrer > Daten 1 > Vorname|Geben Sie hier den Vornamen ein.|LVIMP.TXT|P
Magellan:  Lehrer > Daten 1 > Geboren am|Geben Sie hier das Geburtsdatum ein.|LVIMP.TXT|P
Magellan:  Lehrer > Daten 1 > Geschlecht|Geben Sie hier das Geschlecht ein.|LVIMP.TXT|P
DaVinci Stundenplan    Lehrer > Soll-Berechnung    bezahlter Mehrunterricht|Geben Sie die Mehrarbeitsstunden für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechende Soll-Ist-Schlüssel (Kürzel = „Mehr“).|LVIMP.TXT|B
DaVinci Stundenplan  Lehrer > Soll-Berechnung    Ermäßigungen|Geben Sie die Ermäßigungsstunden pro Ermäßigungsart für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechende Soll-Ist-Schlüssel. |LVIMP.TXT|B
DaVinci Stundenplan  Lehrer > Soll-Berechnung   Arbeitskonto|Geben Sie das Arbeitszeitkonto für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechende Soll-Ist-Schlüssel (Kürzel = „Arbeit“).|LVIMP.TXT|B
DaVinci Stundenplan  Lehrer > Soll-Berechnung  Ausgleich Arbeitskonto|Geben Sie den evtl. Ausgleich für das Arbeitszeitkonto für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechende Soll-Ist-Schlüssel (Kürzel = „Ausgl“).|LVIMP.TXT|B
DaVinci Stundenplan  Lehrer > Veranstaltungsliste  Stunden pro Schulgliederung|Die Unterrichtsstunden pro Schulgliederung ergeben sich aus der Veranstaltungsliste des Lehrers. Der Plan muss dazu nicht gesetzt sein.|LVIMP.TXT|P

### Schülerdaten

Diese Angaben beziehen sich auf das aktuelle Schulhalbjahr.

#### Angaben beim Mandanten

Die folgenden Angaben müssen beim Mandanten in Magellan gemacht werden, damit die Schülerdatei SIL.TXT erzeugt werden kann.

Angabe gemäß Statistik |Angabe in Magellan
--|--
Schulnummer| Ansicht/Mandant/Schulnummer

#### Angaben bei Schülern

Die folgenden Angaben müssen bei Schülern in Magellan gemäß den offiziellen Statistikvorgaben gemacht werden, damit die Schülerdatei SIL.TXT erzeugt werden kann.

Angabe gemäß Statistik |Angabe in Magellan
--|--
Geburtsdatum |Ansicht > Schüler > Daten1 > Geburtsdatum
Geschlecht |Ansicht > Schüler > Daten1 > Geschlecht
Staatsangehörigkeit |Ansicht > Schüler > Daten2 > Staatsangeh. 1
Beruf |Ansicht > Schüler > Ausbildung > Beruf
Besonderheiten des Bildungsganges |Ansicht > Schüler > Merkmale > Merkmal A1
Ausbildungsbeginn |Ansicht > Schüler > Ausbildung > Ausbildung von
Zuletzt besuchter Bildungsgang |Ansicht > Schüler > Zugang-Abgang > Bereits besuchte Schule > Schulform
Höchster erworbener Abschluss |Ansicht > Schüler > Daten 2 > AbschlussABS
Wiederholer der Klassenstufe |Ansicht > Schüler > Laufbahn > Wiederholer
Konfession |Ansicht > Schüler > Daten 1 > Konfession
Teilnahme am Zusatzangebot Fachhochschule |Ansicht > Schüler > Zeugnis > Details > Teilnahme an Zusatzangebot
Zuständiger Landkreis > kreisfreie Stadt für die Beschulung |Ansicht > Schüler > Gemeindenummer bzw. Ansicht > Betriebe > Gemeindenummer
Schulinternes Ordnungsmerkmal |Ansicht > Schüler > Merkmale > Merkmal B1
Umschüler |Ansicht > Schüler > Daten 4 > Förderung (wenn gefüllt, dann Umschüler)
Umschulträger| Ansicht > Schüler > Daten 4 > Förderung
Entgelt pro Monat| Ansicht > Schüler > Daten 4 > Förderbetrag
Nachname |Ansicht > Schüler > Daten 1 > Nachname
Vorname| Ansicht > Schüler > Daten 1 > Vorname
Budget-Beitrag Theorie des Bildungsganges |Ansicht > Schüler > Merkmale > Merkmal B2
Budget-Beitrag Fachpraxis d. Bildungsganges |Ansicht > Schüler > Merkmale > Merkmal B3
Berufliche Vorbildung |Ansicht > Schüler > Merkmale > Merkmal A3
Sprache bzw. Sprachengruppe bei überwiegend nichtdeutscher Verkehrssprache in der Familie. |Ansicht > Schüler > Daten 2 > Sprachgruppe
