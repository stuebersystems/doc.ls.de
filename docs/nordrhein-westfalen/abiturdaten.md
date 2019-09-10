# Abiturdaten der ABI.TXT

## Voraussetzungen zum Export

[Beachten Sie bitte die Mindesteingaben für die Statistik!](https://doc.ls.stueber.de/nordrhein-westfalen/abs-bbs/#voraussetzungen-für-alle-statistikdaten)

Schulform                                          | MAGELLAN | Beschreibung
-------------------------------------------------- | -------- | ------------
`Schüler > Abschluss > Abschluss 1 > Abschlussart` | **Für Berufskollegs**:<br/>Es werden nur Schüler berücksichtigt, die das Abitur bestanden und dementsprechend, das Statistikfeld `Pruefstatus` auf Wert 1 gesetzt haben. Das Feld berechnet sich gemäß der Eingaben in `MAGELLAN > Abitur > Prüfung > Status` und dessen Gliederung einer der folgenden lautet: D01, D02, D05, D06.

## Dateneingabe

Art               | Inhalt
----------------- | ------
**Statistikfeld** | **ldNR**
Schulform         | Alle
Datenfeld         | MAGELLAN: Wird beim Export berechnet.
Beschreibung      | Schulinterne Nummer des Schülers. Wird von MAGELLAN automatisch erzeugt. Achtung: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN.
**Statistikfeld** | **Bildungsgang**
Schulform         | WB
Datenfeld         | MAGELLAN: Klassen > Daten 1 > Schulart [Schularten]
Beschreibung      | Die Schulart der Klasse gibt an, ob es sich um ein Abendgymnasium, Abendrealschule oder Kolleg handelt. Geben Sie den entsprechenden Wert an.
**Statistikfeld** | **Gliederung**
Schulform         | BK, GY, GE
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]<br/>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | ***ABS***: Gymnasien/Gesamtschulen geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **Fachklasse**
Schulform         | BK
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]
Beschreibung      | Die Schulgliederung wird anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung, alles danach ergibt die Fachklasse. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **Zeugnis**
Schulform         | BK
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang
Beschreibung      | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für die Statistik erfasst. ***Wichtig:*** Es sind nur Abgangsarten/Abschlüsse mit Abitur oder fachgebundenem Abitur zulässig.
**Statistikfeld** | **Geburtsdatum**
Schulform         | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsdatum
Beschreibung      | Geben Sie das Geburtsdatum des Schülers ein.
**Statistikfeld** | **Geschlecht**
Schulform         | BK
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie das Geschlecht des Schülers aus. ***WICHTIG***: MAGELLAN 7 unterstützt das neue Geschlecht D = divers. Dieses wird durch die Statistik in diesem Jahr noch nicht offiziell unterstützt. In Absprache mit dem Statistikamt wird der zukünftige Schlüssel 5 ausgespielt und vom Amt nicht beanstandet, sollten sie das neue Geschlecht in MAGELLAN verwenden.
**Statistikfeld** | **LK1**
Schulform         | GE, GY
Datenfeld         | MAGELLAN: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als LK1 wird das Fach erkannt, das mit dem Fachstatus 1PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Statistikfeld** | **LK2**
Schulform         | GE, GY
Datenfeld         | MAGELLAN: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als LK2 wird das Fach erkannt, das mit dem Fachstatus 2PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Statistikfeld** | **GKS**
Schulform         | GE, GY
Datenfeld         | MAGELLAN: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als GKS wird das Fach erkannt, das mit dem Fachstatus 3PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Statistikfeld** | **GKM**
Schulform         | GE, GY
Datenfeld         | MAGELLAN: Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus]
Beschreibung      | Als GKM wird das Fach erkannt, das mit dem Fachstatus 4PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter `Schüler > Zeugnis > Fächer` und diese Daten dann per Synchronisation in das Modul Abitur übertragen.
**Statistikfeld** | **Abiturnote**
Schulform         | Alle
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussnote
Beschreibung      | Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist.
**Statistikfeld** | **Staatsang - Staatsangehörigkeit (Staatsangehörigkeiten)**
Schulform         | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1 [Staatsangehörigkeiten]
Beschreibung      | Wählen Sie die Staatsangehörigkeit des Schülers aus.
**Statistikfeld** | **Pruefstatus**
Schulform         | Alle
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Allgemein > Versetzungsart [Versetzungsarten]<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart [Abschlussarten]<br/>Abitur > Prüfung > Status
Beschreibung      | Der Prüfstatus gibt an, ob ein Schüler das Abitur bestanden hat, bzw. zugelassen wurde oder vorher freiwillig zurückgetreten ist. Der freiwillige Rücktritt wird als Versetzungsart angegeben. Die anderen Werte werden entweder über den Status des Abiturmoduls ermittelt, wobei der Status „Gesamtqualifikation nicht erreicht“ als „Nicht zum Abitur zugelassen“ interpretiert wird. Wenn Sie das Abiturmodul nicht einsetzen, können Sie die Werte über die Abschlussart des 1. Abschlusses angeben.
