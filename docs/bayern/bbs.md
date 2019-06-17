# BBS Statistik

> Die Legende zu den nachstehenden Tabellen finden Sie [HIER](../legende-statistikfelder.md).

## Grundsätzlich

Mit daVinci bzw. Magellan können die folgenden für die Statistik relevanten Daten erzeugt werden

| Daten | Voraussetzung |
| :--- | :--- |
| Lehrerdaten | daVinci-Lizenz |
| Schüler- \/Abgängerdaten | Magellan- und daVinci-Lizenz |
| Klassendaten | Magellan und daVinci-Lizenz |



Nachfolgend finden Sie eine Beschreibung für die Erzeugung der Schüler-\/Abgängerdaten und Klassendaten für die Herbststatistik 2004\/2005. Zurzeit können nur Schüler-\/Abgänger- bzw. Klassendaten für die Schulart „Berufsschule“ \(Schlüssel=31\) erzeugt werden. Die weiteren Schularten sind zurzeit in Vorbereitung.

## Vorgehensweise 


Die grundlegende Vorgehensweise zum Erstellen der Statistik ist die folgende:
1.    Überprüfen Sie in Magellan, ob Sie alle Daten richtig eingetragen haben bzw. tragen Sie noch fehlende Angaben nach. Dies gilt sowohl für den aktuellen Zeitraum \(1. Halbjahr 2004\/2005\) als auch für die vorangegangenen Zeiträume seit der Vorjahresstatistik \(1. und 2. Halbjahr 2003\/2004\).
2.    Überprüfen Sie in daVinci, ob Lehrer, Klassen und Fächer mit Magellan abgeglichen worden sind. 
3.    Übertragen Sie in Magellan die Daten des aktuellen Zeitraums \(1. Halbjahr 2004\/2005\) und der vorangegangenen Zeiträume \(1. und 2. Halbjahr 2003\/2004\) in das Magellan-Datawarehouse.
4.    Starten Sie den Magellan-DWH-Explorer und erstellen Sie dort mit Hilfe des Statistikassistenten für Bayern die geforderten Dateien.
5.    Sie können sich den Inhalt der Dateien mit Hilfe eines Texteditors anzeigen lassen.

## Datenüberprüfung 

#### Datenüberprüfung in Magellan

Bevor Sie die Daten von Magellan ins Datawarehouse übertragen, sollten Sie kontrollieren, ob alle geforderten Daten in Magellan richtig eingetragen sind.

#### Datenüberprüfung in daVinci

Bevor Sie die Daten von daVinci ins Datawarehouse übertragen, sollten Sie kontrollieren, ob alle geforderten Daten in daVinci richtig eingetragen sind. Außerdem müssen die Stammdaten mit Magellan abgeglichen worden sein, damit später im Datawarehouse die Lehrer, Klassen und Fächer zueinander passen.

## Aktive Schüler 


| Ansicht | Feld | Eingabe |
| :--- | :--- | :--- |
| Ansicht Mandant | Schulnummer | Geben Sie hier \(falls noch nicht geschehen\) Ihre 4-stellige Schulnummer bzw. Dienststellennummer ein, mit der alle Dateien signiert werden. |
| Ansicht Klassen | Statistikkürzel | Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie unter Statistikkürzel nichts eintragen. |
| Ansicht Klassen | Schulart | Geben Sie hier die Schulart ein. Grundlage hierfür ist das Schlüsselverzeichnis Schularten. Hinweis: Zurzeit werden nur Klassen mit dem Schulart 31 \(=Berufsschule\) unterstützt. |
| Ansicht Klassen| Unterrichtsart | Geben Sie hier die Unterrichtsform ein. Grundlage hierfür ist das Schlüsselverzeichnis Organisationen. |
| Ansicht Klassen| Beruf | Geben Sie hier die Fachklassennummer für die Klasse ein. Grundlage hierfür ist das Schlüsselverzeichnis Berufe. |
| Ansicht Klassen| Jahrgang | Geben Sie hier die Jahrgangsstufe der Klasse ein. Hinweis: Der Jahrgang ist pro Zeitraum der Klasse anzugeben. |
| Ansicht Klassen| Merkmal A1 | Geben Sie hier die Klassenart der Klasse ein. Grundlage hierfür ist das Schlüsselverzeichnis Klassenmerkmale \(Bereich A1\). |
| Ansicht Klassen| Merkmal B1 | Geben Sie hier die laufende Nummer der Außenstelle der Klasse an. |
| Ansicht Klassen| Merkmal B2 | Geben Sie hier den Regionalschlüssel der Klasse an. |
| Ansicht Klassen| Merkmal B3 | Geben Sie hier die Zahl der Unterrichtswochen im Schuljahr bei Blockunterricht an. |
| Ansicht Klassen| Merkmal B4: | Geben Sie hier die Zahl der Blöcke im Schuljahr bei Blockunterricht an. |
| Ansicht Schüler | Triviale Angaben | Darunter fallen Geschlecht und Geburtsdatum. |
| Ansicht Schüler | Staatsangehörigkeit 1 | Geben Sie hier die Nationalität ein. Grundlage hierfür ist das Schlüsselverzeichnis „Staatsangehörigkeiten“. |
| Ansicht Schüler | Konfession | Geben Sie hier die Religionszugehörigkeit der Schülers ein. Grundlage hierfür ist das Schlüsselverzeichnis „Konfessionen“. |
| Ansicht Schüler | Merkmal A1 | Geben Sie hier die im Vorjahr besuchte Schulart ein. Grundlage hierfür ist das Schlüsselverzeichnis „Schülermerkmale \(Bereich A1\)“. |
| Ansicht Schüler | Höchster Abschluss ABS | \(Vorbildung\) Geben Sie hier den höchsten erreichten Abschluss ein. Grundlage hierfür ist das Schlüsselverzeichnis „Abschlüsse \(Extern\)“. |
| Ansicht Schüler | Merkmal A2 |\(Vorbildung\) Geben Sie hier die vor dem höchsten Abschluss besuchte Schulart ein. Grundlage hierfür ist das Schlüsselverzeichnis „Schülermerkmale“ \(Bereich A2\). |
| Ansicht Schüler | Rel.-Teilnahme | Geben Sie hier die Teilnahme am Religionsunterricht an. Grundlage hierfür ist das Schlüsselverzeichnis „Religion \(Teilnahmen\)“. |
| Ansicht Schüler | Merkmal A3 | Geben Sie hier die Unterbringung ein. Grundlage hierfür ist das Schlüsselverzeichnis „Schülermerkmale“ \(Bereich A3\). |
| Ansicht Schüler | Merkmal A4  |Geben Sie hier das Gastschulverhältnis ein. Grundlage hierfür ist das Schlüsselverzeichnis „Schülermerkmale“ \(Bereich A4\). |
| Ansicht Schüler | Beruf | Geben Sie hier die Berufsnummer ein. Grundlage hierfür ist das Schlüsselverzeichnis „Berufe“. |
| Ansicht Schüler | Fremdsprachen | Geben Sie hier die Fremdsprachen des Schülers an. Sie können bis zu vier Fremdsprachen zuweisen. Grundlage für die Fächerauswahl ist das Schlüsselverzeichnis Fächer, wobei jedem eingetragenen Fach für eine Fremdsprache die Kategorie „Fremdsprache“ im Schlüsselverzeichnis zugeordnet werden muss. |

# Abgänger/Absolventen 


Die folgenden Angaben müssen zusätzlich bei den Entlassenen \(Abgänger\/Absolventen\) eingetragen werden. Da sich diese Angaben auf das vergangene Schuljahr beziehen, müssen Sie darauf achten, dass Sie den richtigen Zeitraum \(1. bzw. 2. Schulhalbjahr 2003\/2004\) einstellen.

| Ansicht | Feld | Eingabe |
| :--- | :--- | :--- |
| Ansicht Schüler | Abgang am | Geben Sie hier an, wann der Schüler abgegangen ist. |
| Ansicht Schüler| Abgangsart | Geben Sie hier an, aus welcher Jahrgangsstufe die Übertritte\/Abgänge erfolgen. Grundlage hierfür ist das Schlüsselverzeichnis „Abgangsarten \(Schüler\)“. |
| Ansicht Schüler| Merkmal A5 | Geben Sie hier die Zeitform des an der Schule zuletzt besuchten Unterrichts an. Grundlage hierfür ist das Schlüsselverzeichnis „Schülermerkmale“ \(Bereich A5\). |
| Ansicht Schüler| Abschluss 1 | Geben Sie hier den durch den Besuch der Schule erreichten berufsbildenden Abschluss an. Grundlage hierfür ist das Schlüsselverzeichnis „Abschlüsse \(Intern\)“. |
| Ansicht Schüler| Abschluss 2 | Geben Sie hier den durch den Besuch der Schule erreichten allgemeinbildenden Abschluss an. Grundlage hierfür ist das Schlüsselverzeichnis „Abschlüsse \(Intern\)“. |

# Nicht-Schülerprüfung 
Die folgenden Angaben müssen zusätzlich bei den Teilnehmern der Nichtschülerprüfung eingetragen werden. Da sich diese Angaben auf das vergangene Schuljahr beziehen, müssen Sie darauf achten, dass Sie den richtigen Zeitraum (1. bzw. 2. Schulhalbjahr 2003/2004) einstellen.

Ansicht | Feld | Eingabe 
 --- | --- | --- 
Schüler| Aufnahmeprüfung | Geben Sie hier den erworbenen Abschluss der Nicht Schülerprüfung an. Grundlage hierfür ist das Schlüsselverzeichnis „Aufnahmeprüfungen“. 

## Veranstaltungsliste in DAVINCI 

Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.

## Schritte im Datawarehouse 


## Übertrag aus MAGELLAN 

Sie können alle Daten direkt aus Magellan heraus in das Magellan-Datawarehouse übertragen.
6.    Wählen Sie in Magellan die Ansicht Datawarehouse aus.
7.    Klicken Sie dort unterhalb von Extras auf Starten.
8.    Der Importassistent für das Magellan-Datawarehouse wird gestartet. Sie müssen sich jetzt erneut bei Magellan mit Ihrer Kennung und Ihrem Kennwort anmelden.
9.    Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und  Zeitraum  aus.
10.    Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

Sie müssen diesen Vorgang mehrfach ausführen, um die Daten sowohl aus dem aktuellen Zeitraum \(1. Halbjahr 2004\/2005\) als auch aus den beiden vorangegangenen Zeiträumen \(1. und 2. Halbjahr 2003\/2004\) zu übertragen.

## Übertrag aus DAVINCI 
Über die Archivierungsfunktion in daVinci-Stundenplan werden die Daten der aktuellen daVinci-Plandatei in das Magellan Datawarehouse übertragen.
1.    Starten Sie daVinci-Stundenplan mit Ihrer Plandatei.
2.    Wählen Sie Extras und dann Archivieren.
3.    Bestätigen Sie die Sicherheitsabfrage. Die Daten werden jetzt in eine Schuldatentransferdatei exportiert, anschließend wird der Importassistent für das Magellan-Datawarehouse gestartet. Sie müssen sich jetzt bei Magellan mit Ihrer Kennung und Ihrem Kennwort anmelden.
4.    Klicken Sie auf Weiter und wählen Sie den passenden Mandanten und Zeitraum aus. Für die Statistik wäre dies der Zeitraum ab 01.08.2004.
5.    Klicken Sie auf Weiter und dann auf Starten. Die Daten werden jetzt in das Magellan Datawarehouse übertragen.

## Datenüberprüfung 


Mit Hilfe des Magellan DWH Explorer können Sie sich den Inhalt des Magellan Datawarehouse anzeigen lassen. Gehen Sie dabei wie folgt vor:
1.    Klicken Sie auf Start, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan DWH Explorer.
2.    Wählen Sie die Ansicht Datenbestand aus.
3.    Wählen Sie den passenden Mandanten aus und tragen Sie einen passenden Zeitpunkt ein. Möchten Sie die Abgänger aus dem alten Schuljahr betrachten, so tragen Sie als Zeitpunkt beispielsweise den letzten Schultag ein. Möchten Sie die aktuellen Schuldaten betrachten, tragen Sie das heutige Datum ein. Sie können nun durch Wechseln der Registerkarten die eingetragenen Klassen, Schüler, Lehrer usw. betrachten.

## Statistikerstellung 

Mit Hilfe des Magellan DWH Explorer können Sie auf das Magellan Datawarehouse zugreifen und die geforderten Statistikdateien erstellen. Gehen Sie dabei wie folgt vor:
1.    Klicken Sie auf Start, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf Magellan DWH Explorer.
2.    Wählen Sie die Ansicht Auswertungen aus.
3.    Wählen Sie unter Landesstatistik die Option Statistikformat für Bayern BBS aus und klicken Sie auf Starten.
4.    Folgen Sie nun den Anweisungen des Assistenten. Sie müssen dabei den Mandanten auswählen, das Erhebungszeitpunkt, den Abgängerzeitraum der Abgänger\/Absolventen\/Nichtschüler angeben sowie den Ordner wählen, in dem die Dateien erzeugt werden soll.

## Erhebungszeitpunkt 

Der Erhebungszeitpunkt definiert den Stichtag, auf den sich die Statistik bezieht. Dieses Datum ist für die aktuellen Daten anzugeben und sollte in der vom Statistikamt vorgegebenen Woche liegen.



