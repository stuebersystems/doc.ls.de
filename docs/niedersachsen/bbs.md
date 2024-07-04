
# Niedersachsen - BBS

## Lizenz und Version

Für das Erzeugen der Schnittstellendatei wird die jährliche Lizenz für das Modul "Modul LANDESSTATISTIK Niedersachsen BBS" benötigt. Damit können die Daten für die amtliche Statistik Niedersachsen (IZN-Stabil) erzeugt werden. Zusätzlich ist Support zum Modul und das jeweilige Jahr enthalten.



## Grundsätzlich

Mit DaVinci und Magellan können Sie alle Datensätze erstellen, die für die Erhebung der amtlichen Landsschulstatistik benötigt werden.  Wenn Sie nur DaVinci besitzen, können Sie nur einen Teil der Statistik erzeugen.Mit DaVinci bzw.

!!! info "Hinweis"

     Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Magellan können die folgenden Dateien erzeugt werden

Datei| Beschreibung |Voraussetzung
--|--|--
STD.TXT |Stundenplandaten |DaVinci-Lizenz
SIL.TXT |Aktuelle Schülerdaten |Magellan- und DaVinci-Lizenz
ABL.TXT |Abgängerdaten |Magellan- und DaVinci-Lizenz
LV.TXT| Lehrerdaten |Magellan- und DaVinci-Lizenz

Die erzeugten Dateien können dann vom Statistikprogramm BBS-Planung weiterverarbeitet werden.

## Allgemeines

Die Schüler-, Abgänger und Lehrerdaten werden aus DaVinci und Magellan erzeugt. Dazu werden zunächst die Daten aus DaVinci und Magellan in das Magellan-Datawarehouse übertragen. Von dort aus erstellen Sie dann die drei Dateien SIL.TXT, ABL.TXT und LV.TXT und diese später nach BBS-Planung zu importieren.

## Vorgehensweise

Die grundlegende Vorgehensweise zum Erstellen der Statistik ist die folgende:

1. Überprüfen Sie in Magellan, ob Sie alle Daten richtig eingetragen haben bzw. tragen Sie noch fehlende Angaben nach. Dies gilt sowohl für den aktuellen Zeitraum (1. Halbjahr) als auch für die vorangegangenen Zeiträume seit der Vorjahresstatistik (1. und 2. Halbjahr ).
2. Überprüfen Sie in DaVinci, ob Lehrer, Klassen und Fächer mit Magellan abgeglichen worden sind. Überprüfen Sie, ob bei allen Lehrern die Soll-Berechnung richtig erfasst wurde.
3. Übertragen Sie in Magellan die Daten des aktuellen Zeitraums (1. Halbjahr) und der vorangegangenen Zeiträume (1. und 2. Halbjahr) in das Magellan-Datawarehouse.
4. Übertragen Sie in DaVinci die Daten der aktuellen Stundenplandatei in das Magellan-Datawarehouse.
5. Starten Sie den Magellan-DWH-Explorer und erstellen Sie dort die mit Hilfe des Statistikassistenten für Niedersachsen BBS die geforderten Dateien für BBS-Planung.
6. Importieren Sie die Dateien in BBS-Planung.

## Statistikschlüssel aktualisieren

Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](https://doc.ls.stueber.de/schluesselverzeichnisse/).

## Stundenplandaten

Die Stundenplandaten werden ausschließlich von DaVinci erzeugt. Dazu exportiert DaVinci Daten aus der aktuellen Stundenplandatei in die Datei STD.TXT, die Sie dann in BBS-Planung einlesen können.

## Notwendige Angaben für die Statistik

Die folgenden Angaben müssen in DaVinci gemäß den offiziellen Statistikvorgaben gemacht werden. Bitte beachten Sie unbedingt die maximal zulässige Länge für Klassen-, Lehrer- und Fachkürzel. 


!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Angabe gemäß Statistik |Angabe in DaVinci
--|--
Schulnummer |Wird im Dialogfenster „Exportieren“ abgefragt
Klassenkürzel| Klassenkürzel im Stammdatenfenster auf Registerkarte „Klassen“
Statistische Bezeichnung des Fachs| Spalte „Schlüssel“ im Stammdatenfenster auf Registerkarte „Fächer“
Sollstunden |Spalte „Dauer“ bei Stundentafeln
Iststunden |Spalte „Dauer/W“ in der Unterrichtsliste des Planungsfens-ter
Lehrerkürzel| Lehrerkürzel im Stammdatenfenster auf Registerkarte „Lehrer“
Qualifizierung der Unterrichtsstunde |siehe folgendes Kapitel

## Qualifizierung der Unterrichtsstunden

Unterrichtsstunden müssen korrekt qualifiziert werden. Sie müssen dazu die laut Statistik vorgegebenen Angaben in  den Schlüsselverzeichnissen „Unterrichtsarten“ und „Fachstati“ in DaVinci machen (klicken Sie in DaVinci auf „Extras > Schlüsselverzeichnisse“). Entscheidend ist dabei jeweils der Schlüssel. Er wird exportiert, nicht das Kürzel! Der Schlüssel muss gemäß der Ausfüllanleitung eingegeben werden. 

Folgende Unterrichtsarten werden von DaVinci benutzt: 

Unterrichtsart Schlüssel| wird exportiert als 
--|--
Kurs|SO
LK |LK
GK |GK
FP |FP

Alle übrigen Qualifizierungen müssen als Fachstati eingegeben werden. Der Schlüssel muss gemäß der Ausfüllanleitung eingegeben werden.
##Stunden-Datensätze aus DaVinci exportieren

So exportieren Sie in DaVinci die Stunden-Datensätze

1. Klicken Sie auf Extras|Exportieren. Das Dialogfenster Exportieren öffnet sich.
2. Geben Sie den Namen der Exportdatei an. Die Datei sollte die Endung .STD haben.
3. Stellen Sie unter Dateityp Niedersachsen Statistik BBS ein.
4. Das Eingabefeld für die Schulnummer erscheint unten. Geben Sie dort Ihre Schulnummer ein.
5. Klicken Sie auf OK. Die Datei STD.TXT mit den Stunden-Datensätzen wird erzeugt. 

## Stundenplandatei nach BBS-Planung importieren

Die erzeugte Statistikdatei STD.TXT muss nach BBS-Planung importiert werden. Dazu gehen Sie wie folgt vor.

1. Starten Sie BBS-Planung
2. Klicken Sie auf „Verwaltung“ und dann auf „Statistik“.
3. Klicken Sie zum Import der Datei auf das entsprechende graue Feld in der Zeile „importieren“ in der entsprechenden Spalte.

## Klassendaten

Die folgenden Angaben müssen bei Klassen in Magellan gemäß den offiziellen Statistikvorgaben gemacht werden, damit die Schülerdatei SIL.TXT erzeugt werden kann.


!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Angabe gemäß Statistik |Angabe in Magellan|Anmerkung
--|--|--
Klassenkürzel |Ansicht > Klassen > Daten1 > Statistikkürzel|
Schulform |Ansicht > Klassen > Schulform|
Beruf der Schüler |Ansicht > Klassen > Beruf |nur wenn nicht bei Beruf des Schülers eingetragen
Klassenstufe |Ansicht > Klassen >  Zeiträume > Zeitraum > Klassenstufe |Angaben müssen pro Zeitraum der Klasse erfolgen
Organisation| Ansicht > Klassen > Daten1 > Organisation|
Berufsgruppe |Ansicht > Klassen > Merkmale > Merkmal B1|enthält die Berufsgruppe gemäß Klassenbildungserlass. Muss 8-stellig sein.
Stelle 1-2| Schulform|
Stelle 3|Berufsfeld > Fachrichtung|
Stelle 4-5| frei definierbar|richtet sich danach, welche Bildungsgänge gemeinsam unterrichtet werden können
Stelle 6| Klassenstufe|
Stelle 7| Unterrichtsorganisation|
Stelle 8| Besonderheiten des Bildungsganges|

## Abgängerdaten

Diese Angaben beziehen sich auf das vorangegangene Schuljahr. Es werden dazu alle Schüler des 1. und 2. Halbjahres berücksichtigt.

### Angaben bei Klassen

Die folgenden Angaben müssen bei Klassen in Magellan gemäß den offiziellen Statistikvorgaben gemacht werden, damit die Abgängerdatei ABL.TXT erzeugt werden kann.

Angabe gemäß Statistik |Angabe in Magellan
--|--
Schulform |Ansicht > Klassen > Schulform
Beruf der Schüler |Ansicht > Klassen > Beruf (nur wenn nicht bei Beruf des Schülers eingetragen)
Klassenstufe |Ansicht > Klassen >  Zeiträume > Zeitraum > Klassenstufe Angaben müssen pro Zeitraum der Klasse erfolgen
Organisation| Ansicht > Klassen > Daten1 > Organisation

### Angaben bei Schülern


!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Die folgenden Angaben müssen bei Schülern in Magellan gemäß den offiziellen Statistikvorgaben gemacht werden, damit die Abgängerdatei ABL.TXT erzeugt werden kann.

Angabe gemäß Statistik|Angabe in Magellan
--|--
Geburtsdatum|Ansicht > Schüler > Daten1 > Geburtsdatum
Geschlecht|Ansicht > Schüler > Daten1 > Geschlecht
Staatsangehörigkeit|Ansicht > Schüler > Daten2 > Staatsangeh. 1
Beruf|Ansicht > Schüler > Ausbildung > Beruf
Besonderheiten des Bildungsganges|Ansicht > Schüler > Merkmale > Merkmal A1
Ausbildungsbeginn|Ansicht > Schüler > Ausbildung > Ausbildung von
Zuletzt besuchter Bildungsgang|Ansicht > Schüler > Zugang-Abgang > Bereits besuchte Schule > Schulform
Höchster erworbener Abschluss|Ansicht > Schüler > Daten 2 > AbschlussABS
Entlassungsdatum|Ansicht > Schüler > Zugang-Abgang > Abgang am
Zuständiger Landkreis > kreisfreie Stadt für die Beschulung|Ansicht > Schüler > Gemeindenummer bzw. Ansicht > Betriebe > Gemeindenummer
Abschluss|Ansicht > Schüler > Zugang-Abgang > Abgangsart
Nachname|Ansicht > Schüler > Daten 1 > Nachname
Vorname|Ansicht > Schüler > Daten 1 > Vorname
Berufliche Vorbildung|Ansicht > Schüler > Merkmale > Merkmal A3
Aufgenommen Ausbildung > Beruf nach Abschluss d. beruf. Schule|Ansicht > Schüler > Merkmale > Merkmal A5
Angenommen Ausbildung > Beruf ein Jahr nach Verlassen d. beruf. Schule|Ansicht > Schüler > Merkmale > Merkmal A6
Erreichter beruflicher Abschluss in der Berufsschule oder begleitend zum Schulbesuch|Ansicht > Schüler > Merkmale > Merkmal A4
Sprache bzw. Sprachengruppe bei überwiegend nichtdeutscher Verkehrssprache in der Familie|Ansicht > Schüler > Daten 2 > Sprachgruppe

## Lehrerdaten

Diese Angaben beziehen sich auf das aktuelle Schulhalbjahr (1. HJ. des aktuell laufenden Schuljahres).

### Angaben in Magellan


!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Die folgenden Angaben müssen bei Lehrern in Magellan gemacht werden, damit die Lehrerdatei LV.TXT erzeugt werden kann.

Angabe gemäß Statistik|Angabe in Magellan
--|--
Stammschule|Ansicht > Lehrer > Merkmale > Merkmal A3 mit den Werten<br>1=Stammschule<br>2=Nebenschule
Nach- und Vorname|Ansicht > Lehrer > Daten1 > Nachname bzw. Vorname
Geschlecht|Ansicht > Lehrer > Daten 1 > Geschlecht
Staatsangehörigkeit|Ansicht > Lehrer > Daten 1 > Staatsangeh
Geburtsdatum|Ansicht > Lehrer > Daten 1 > Geboren am
Beschäftigungsverhältnis|Ansicht > Lehrer > Daten 2 > Besch-verh.
Konfession|Ansicht > Lehrer > Daten 1 > Konfession
Lehramt|Ansicht > Lehrer > Daten 3 > Lehrämter<br>mit Lehramtstyp=“Lehramt“
Fach > Fachrichtung|Ansicht > Lehrer > Daten 3 > Lehrämter<br>mit Lehramtstyp=Lehrbefähigung“
Zugangsgrund|Ansicht > Lehrer > Daten2 > Zugangsart
Zugangsjahr|Ansicht > Lehrer > Daten2 > Zugang am
Abgangsgrund|Ansicht > Lehrer > Daten2 > Abgangsart
Abgangsjahr|Ansicht > Lehrer > Daten2 > Zugang am
Merkmal Theorielehrkraft > Fachlehrkraft > Fachpraxislehrkraft|Ansicht > Lehrer > Merkmale > MerkmalA1
Abordnungsstelle 1|Ansicht > Lehrer > Daten 3 > Abordnung 1
Abordnungsstelle 2|Ansicht > Lehrer > Daten 3 > Abordnung 2
Funktionsstelle|Ansicht > Lehrer > Merkmale > MerkmalA2

### Angaben in DaVinci


!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Die folgenden Angaben müssen bei der Lehrer-Soll-Berechnung pro Lehrer in DaVinci gemacht werden, damit die Lehrerdatei LV.TXT erzeugt werden kann.

Eingabe|Anmerkung
--|--
Regel-Vertragsstundenmaß|Geben Sie die Regelstunden für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechenden Soll-Ist-Schlüssel (Kürzel = „REGEL“; Typ = „P“; Bezeich-nung frei wählbar).
Ermäßigungsstunden/-gründe|Geben Sie die Ermäßigungsstunden für jeden Lehrer in seiner Soll-Berechnung an. Grundlage sind die entspre-chenden Soll-Ist-Schlüssel (Kürzel = „ERM0100“ ... „ERM9900“, mit Ausnahme von „ERM28“ und „ERM29“ ; Typ = „-“ ; Bezeichnung frei wählbar).
Stunden an anderer Schule|Geben Sie die Abgabestunden an andere Schulen für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechenden Soll-Ist-Schlüssel (Kürzel = „ANDERE“; Typ = „-“; Bezeichnung frei wählbar).
Bezahlter Mehrunterricht|Geben Sie die Mehrunterrichtsstunden für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist der entsprechenden Soll-Ist-Schlüssel (Kürzel = „MEHR“; Typ = „+“; Bezeichnung frei wählbar).
Mehr- oder Minderstunden aus dem Lebensarbeitskonto|Geben Sie die Mehr- oder Minderstunden aus dem Lebensarbeitskonto für jeden Lehrer in seiner Soll-Berechnung an. Grundlage ist die entsprechenden Soll-Ist-Schlüssel Mehrstunden (Kürzel = „LEB+“; Typ = „#“; Bezeichnung frei wählbar) bzw. Minderstunden (Kürzel = „LEB-“; Typ = „#“; Bezeichnung frei wählbar).
Mehr- oder Minderstunden|Geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung an. Grundlage sind die entsprechenden Soll-Ist-Schlüssel für Minderstunden (Kürzel = „ERM28“; Typ = „-“ ; Bezeichnung frei wählbar) bzw. Mehrstunden (Kürzel = „ERM29“; Typ = „+“ ; Bezeichnung frei wählbar) .

## Übertrag ins Datawarehouse

### Übertrag aus Magellan ins Datawarehouse

Sie können alle Daten direkt aus Magellan heraus in das Magellan-Datawarehouse übertragen.

1. Wählen Sie in Magellan die Ansicht Datawarehouse aus.
2. Klicken Sie dort unterhalb von Extras auf Starten.
3. Der Importassistent für das Magellan-Datawarehouse wird gestartet. Sie müssen sich jetzt erneut bei Magellan mit Ihrer Kennung und Ihrem Kennwort anmelden.
4. Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und  Zeitraum aus.
5. Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

Sie müssen diesen Vorgang mehrfach ausführen, um die Daten sowohl aus dem aktuellen Zeitraum (1. Halbjahr) als auch aus den beiden vorangegangenen Zeiträumen (1. und 2. Halbjahr) zu übertragen.

### Übertrag aus DaVinci in das Datawarehouse

Über die Archivierungsfunktion in DaVinci-Stundenplan werden die Daten der aktuellen DaVinci-Plandatei in das Magellan Datawarehouse übertragen.

1. Starten Sie DaVinci-Stundenplan mit Ihrer Plandatei.
2. Wählen Sie Extras und dann Archivieren.
3. Bestätigen Sie die Sicherheitsabfrage. Die Daten werden jetzt in eine Schuldatentransferdatei exportiert, anschließend wird der Importassistent für das Magellan-Datawarehouse gestartet. Sie müssen sich jetzt bei Magellan mit Ihrer Kennung und Ihrem Kennwort anmelden.
4. Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und  Zeitraum aus.
5. Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.
 
## Datenüberprüfung im Datawarehouse

Mit Hilfe des Magellan DWH Explorer können Sie sich den Inhalt des Magellan Datawarehouse anzeigen lassen. Gehen Sie dabei wie folgt vor:

1. Klicken Sie auf Start, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan DWH Explorer.
2. Wählen Sie die Ansicht Datenbestand aus.
3. Wählen Sie den passenden Mandanten aus und tragen Sie einen passenden Zeitpunkt ein. Möchten Sie Sie die Abgänger aus dem alten Schuljahr betrachten, so tragen Sie als Zeitpunkt beispielsweise den letzten Schultag ein. Möchten Sie die aktuellen Schuldaten betrachten, wählen beispielsweise das heutige Datum.

Sie können nun durch Wechseln der Registerkarten, die eingetragenen Klassen, Schüler, Lehrer usw. betrachten.

## Dateiexport aus dem Datawarehouse

Mit Hilfe des Magellan DWH Explorer können Sie auf das Magellan Datawarehouse zugreifen und die geforderten Dateien SIL.TXT, ABL.TXT und LV.TXT für BBS-Planung erzeugen.  Gehen Sie dabei wie folgt vor:

1. Klicken Sie auf Start, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan DWH Explorer.
2. Wählen Sie die Ansicht Auswertungen aus.
3. Wählen Sie unter Landesstatistik die Option Statistikformat für Niedersachsen (BBS) aus und klicken Sie auf Starten.
4. Folgen Sie nun den Anweisungen des Assistenten. Sie müssen dabei den Mandanten auswählen, welche Dateien Sie erstellen möchten (SIL.TXT, ABL.TXT bzw. LV.TXT), den Erhebungszeitpunkt bzw. den Abgängerzeitraum sowie den Ordner, in dem die Dateien erzeugt werden soll.


!!! info "Hinweis"

    Bitte beachten Sie die Unterscheidung zwischen Erhebungszeitpunkt und Abgängerzeitraum

Wert|Hinweis
--|--
Abgängerzeitraum| Der Abgängerzeitraum  definiert den Zeitraum, auf den sich das letzte Schuljahr bezieht. Dieser Zeitraum sollte den gesamten Zeitraum des letzten Schuljahres (1. und 2. Halbjahr) umfassen.
Erhebungszeitpunkt|Der Erhebungszeitpunkt definiert den Stichtag, auf den sich die Statistik bezieht. Dieses Datum ist für die aktuellen Daten anzugeben und sollte in der vom Statistikamt vorgegebenen Woche liegen.

### Dateiimport in BBS-Planung

Die erzeugten Statistikdateien müssen nach BBS-Planung importiert werden. Dazu gehen Sie wie folgt vor.

1. Starten Sie BBS-Planung
2. Klicken Sie auf Verwaltung und dann auf Statistik.
3. Klicken Sie zum Import der Datei auf das entsprechende graue Feld in der Zeile importieren in der entsprechenden Spalte.
