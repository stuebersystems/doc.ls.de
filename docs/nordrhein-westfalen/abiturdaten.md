# Abiturdaten der ABI.TXT

## Voraussetzungen zum Export

Nachstehend beschreiben wir die Angaben, die für ein Ausspielen der Abiturienten mindestens vorausgesetzt werden, die vollständige Liste aller Eintragungen finden Sie im Abschnitt [https://doc.ls.stueber.de/nordrhein-westfalen/abiturdaten/#dateneingabe](https://doc.ls.stueber.de/nordrhein-westfalen/abiturdaten/#dateneingabe).

|Schulform und Beschreibung|
|-- |
|**Für Berufskollegs**:<br/><br/>`Schüler > Laufbahn > Abschluss 1 > Abschlussart`<br/>`Abitur > Prüfung > Status`<br/>`Klassen > Zeiträume > Klassenstufe` <br/><br/>Es werden nur Schüler berücksichtigt, die das Abitur bestanden und dementsprechend, das Exportfeld `Pruefstatus` auf Wert 1 gesetzt haben. <br/>Das Feld berechnet sich gemäß der Eingaben in `Magellan > Abitur > Prüfung > Status` (Gliederungswerte: D01, D02, D05, D06) und der Eingabe unter `Schüler > Abschluss > Abschluss 1 > Abschlussart`. <br/>Bitte beachten Sie auch, dass die Klassenstufe unter Klassen > Zeiträume für die Abschlussklassen mit dem Wert `Q2` gefüllt werden muss.<br/><br/>Bitte beachten Sie zusätzlich die [Mindestangaben](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/#voraussetzungen-fur-alle-daten)!
|**Für Weiterbildungskollegs**:<br/><br/>`Schüler > Abschluss > Abschluss 1 > Abschlussart`<br/>`Abitur > Prüfung > Status`<br/>`Klassen > Zeiträume > Klassenstufe`<br/>`Klassen > Zeiträume > Jahrgang`<br/>`Schüler > Laufbahn > Abschluss 1 > Abschlussart`br/>`Schüler > Daten3 > Verschiedenes > G8/G9`<br/><br/>Es werden nur Schüler berücksichtigt, die das Abitur bestanden und dementsprechend, das Exportfeld `Pruefstatus` auf Wert 1 gesetzt haben. <br/>Das Feld berechnet sich gemäß der Eingaben in `Magellan > Abitur > Prüfung > Status` (Gliederungswerte: D01, D02, D05, D06) und der Eingabe unter `Schüler > Abschluss > Abschluss 1 > Abschlussart`.<br/>Bitte beachten Sie auch, dass die Klassenstufe unter Klassen > Zeiträume für die Abschlussklassen mit dem Wert `Q2` gefüllt werden muss. Es werden Schüler ausgegeben, die in einer Klasse mit der Jahrgangsstufe 12 oder 13 sind (`Klassen > Zeiträume > Jahrgang`) und einen Eintrag unter `Daten3 > G8/G9` haben (G8 = 12 und G9 = Jahrgang 13). <br/>Zum Befüllen des Feldes `G8/G9` steht Ihnen die Sammelzuweisung im `Menü Schüler` auf der Registerkarte `Schüler` zur Verfügung. <br/>Sind G8 als auch G9 Schüler in einer Klasse muss die Klassenstufe (Schlüssel) Q2 unter `Klassen > Zeiträume > Klassenstufe` angegeben werden.<br/><br/>Bitte beachten Sie zusätzlich die [Mindestangaben](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/#voraussetzungen-fur-alle-daten)!
|**Für Gymnasien**:<br/><br/>`Schüler > Daten3 > G8/G9`<br/>`Klassen > Zeiträume > Jahrgang`<br/>`Klassen > Zeiträume > Klassenstufe`<br/><br/>Es werden Schüler ausgegeben, die in einer Klasse mit der Jahrgangsstufe 12 oder 13 sind (`Klassen > Zeiträume > Jahrgang`) und einen Eintrag unter `Daten3 > G8/G9` haben (G8 = 12 und G9 = Jahrgang 13). <br/>Zum Befüllen des Feldes `G8/G9` steht Ihnen die Sammelzuweisung im `Menü Schüler` auf der Registerkarte `Schüler` zur Verfügung. <br/>Sind G8 als auch G9 Schüler in einer Klasse muss die Klassenstufe (Schlüssel) Q2 unter `Klassen > Zeiträume > Klassenstufe` angegeben werden.<br/><br/>Bitte beachten Sie zusätzlich die [Mindestangaben](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/#voraussetzungen-fur-alle-daten)!|

## Dateneingabe

Art               | Inhalt
----------------- | ------
**Exportfeld**    | **ldNR**
Schulform         | Alle
Datenfeld         | Magellan: Wird beim Export berechnet.
Beschreibung      | Schulinterne Nummer des Schülers. Wird von Magellan automatisch erzeugt. Achtung: Es handelt sich hierbei nicht um die Schüler.ID aus Magellan.
**Exportfeld**    | **Bildungsgang**
Schulform         | WB
Datenfeld         | Magellan: Klassen > Daten 1 > Schulart [Schularten]
Beschreibung      | Die Schulart der Klasse gibt an, ob es sich um ein Abendgymnasium, Abendrealschule oder Kolleg handelt. Geben Sie den entsprechenden Wert an.
**Exportfeld**    | **Gliederung**
Schulform         | BK, GY, GE, WB
Datenfeld         | Magellan:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]<br/>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | ***ABS***: Gymnasien/Gesamtschulen und Weiterbildungskollegs geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in Magellan ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Exportfeld**    | **Fachklasse**
Schulform         | BK
Datenfeld         | Magellan:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]
Beschreibung      | Die Schulgliederung wird anhand des Bildungsgangs in Magellan ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung, alles danach ergibt die Fachklasse. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Exportfeld**    | **Zeugnis**
Schulform         | BK
Datenfeld         | Magellan:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 [Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang
Beschreibung      | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für den Export erfasst.<br/>***Wichtig:*** Es sind nur Abgangsarten/Abschlüsse mit Abitur oder fachgebundenem Abitur zulässig.
**Exportfeld**    | **Geburtsdatum**
Schulform         | Alle
Datenfeld         | Magellan: Schüler > Daten 1 > Geburtsdatum
Beschreibung      | Geben Sie das Geburtsdatum des Schülers ein.
**Exportfeld**    | **Geschlecht**
Schulform         | BK
Datenfeld         | Magellan: Schüler > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie das Geschlecht des Schülers aus. <br/>***WICHTIG***: Ab diesem Jahr wird auch offiziell das Geschlecht D = DIVERS vom Amt unterstützt. Zusätzlich ist auch noch der Schlüssel 6 = `Ohne Eintrag (im Geburtsregister)` mit dabei. Dieser Schlüssel wird auch Magellan 10 ausgespielt, wenn das Geschlecht keinen Eintrag enthält.
**Exportfeld**    | **LK1**
Schulform         | GE, GY, WB
Datenfeld         | Magellan: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als LK1 wird das Fach erkannt, das mit dem Fachstatus 1PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Exportfeld**    | **LK2**
Schulform         | GE, GY, WB
Datenfeld         | Magellan: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als LK2 wird das Fach erkannt, das mit dem Fachstatus 2PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Exportfeld**    | **GKS**
Schulform         | GE, GY, WB
Datenfeld         | Magellan: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als GKS wird das Fach erkannt, das mit dem Fachstatus 3PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Exportfeld**    | **GKM**
Schulform         | GE, GY, WB
Datenfeld         | Magellan: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als GKM wird das Fach erkannt, das mit dem Fachstatus 4PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Exportfeld**    | **Abiturnote**
Schulform         | Alle
Datenfeld         | Magellan: Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussnote
Beschreibung      | Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist.
**Exportfeld**    | **Staatsang - Staatsangehörigkeit (Staatsangehörigkeiten)**
Schulform         | Alle
Datenfeld         | Magellan: Schüler > Daten 1 > Staatsangeh. 1 [Staatsangehörigkeiten]
Beschreibung      | Wählen Sie die Staatsangehörigkeit des Schülers aus.
**Exportfeld**    | **Pruefstatus**
Schulform         | Alle
Datenfeld         | Magellan: Schüler > Laufbahn > Allgemein > Versetzungsart [Versetzungsarten]<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart [Abschlussarten]<br/>Abitur > Prüfung > Status
Beschreibung      | Der Prüfstatus gibt an, ob ein Schüler das Abitur bestanden hat, bzw. zugelassen wurde oder vorher freiwillig zurückgetreten ist. Der freiwillige Rücktritt wird als Versetzungsart angegeben. Die anderen Werte werden entweder über den Status des Abiturmoduls ermittelt, wobei der Status „Gesamtqualifikation nicht erreicht“ als „Nicht zum Abitur zugelassen“ interpretiert wird. Wenn Sie das Abiturmodul nicht einsetzen, können Sie die Werte über die Abschlussart des 1. Abschlusses angeben.
