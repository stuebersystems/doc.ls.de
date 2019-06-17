# Abiturdaten der ABI.TXT


[Beachten Sie bitte die Mindesteingaben für die Statistik!](https://doc.ls.stueber.de/nordrhein-westfalen/abs+bbs.html#voraussetzungen-für-alle-statistikdaten)


| Art           | Inhalt                                   |
|---------------|------------------------------------------|
|**Statistikfeld**| **ldNR**                                     |
| Datenfeld     | MAGELLAN:<br/>Wird beim Export berechnet. |
| Beschreibung  | Schulinterne Nummer des Schülers. Wird von MAGELLAN automatisch erzeugt. Achtung: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN. |
|**Statistikfeld**| **Bildungsgang**                             |
| Datenfeld     | MAGELLAN:<br/>Weiterbildungskollegs:<br/>Klassen > Daten 1 > Schulart [Schularten] |
| Beschreibung  | Ab 2017 nur Für Weiterbildungskollegs!Die Schulart der Klasse gibt an,ob es sich um ein Abendgymnasium, Abendrealschule oder Kolleg handelt. Geben Sie den entsprechenden Wert an. |
|**Statistikfeld**| **Gliederung**                               |
| Datenfeld     | MAGELLAN:<br/>Berufskollegs:Klassen > Daten > Bildungsgang <br/>Schüler > Ausbildung > Bildungsgang [Bildgungsgänge] und [Berufsfelder]<br/>Gesamtschulen, Gymnasien:Schüler > Daten 3 > Verschiedenes > Profil [Profile (Schüler)] |
| Beschreibung  | Berufskollegs:<br/>Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN ausgelesen. Lesen Sie dazu die Beschreibung des nächsten Feldes „Fachklasse“.<br/>  Gesamtschulen, Gymnasien:Das Abitur kann in 12 oder 13 Jahren abgeschlossen werden. Wählen Sie dazu im Verzeichnis beim Profil des Schülers entsprechend den Eintrag für G8 oder G9 aus. |
|**Statistikfeld**| **Fachklasse**                               |
| Datenfeld     | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildungsgang[Bildungsgänge]<br/>Schüler > Ausbildung > Von<br/>Schüler > Ausbildung > Bis |
| Beschreibung  | Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, <br/>  müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft. <br/>  Wichtig: Da grundsätzlich der Bildungsgang des Schülers an seiner Ausbildung hängt, müssen das Von- und Bis Datum der Ausbildung in den statistischen Zeitraum passen! |
|**Statistikfeld**| **Zeugnis**                                  |
| Datenfeld     | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang |
| Beschreibung  | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. <br/>  Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für die Statistik erfasst. <br/>  Wichtig: Es sind nur Abgangsarten/Abschlüsse mit Abitur oder fachgebundenem Abitur zulässig. |
|**Statistikfeld**| **Geburtsdatum**                             |
| Datenfeld     | MAGELLAN:<br/>Schüler > Daten 1 > Geburtsdatum |
| Beschreibung  | Geben Sie das Geburtsdatum des Schülers ein. |
|**Statistikfeld**| **Geschlecht**                               |
| Datenfeld     | MAGELLAN:<br/>Klassen > Daten 1 > Geschlecht |
| Beschreibung  | Wählen Sie das Geschlecht des Schülers aus. |
|**Statistikfeld**| **LK1**                                      |
| Datenfeld     | MAGELLAN:<br/>Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus] |
| Beschreibung  | Nur ABS!<br/>  Als LK1 wird das Fach erkannt, das mit dem Fachstatus 1PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter ```Schüler > Zeugnis > Fächer``` <br/>  und diese Daten dann per ynchronisation in das Modul Abitur übertragen.<br/>  Das Feld Fachstatus wird beim Import des Katalogs "00_Fachstati.keys" befüllt. |
|**Statistikfeld**| **LK2**                                      |
| Datenfeld     | MAGELLAN:<br/>Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus] |
| Beschreibung  | Nur ABS!<br/>  Als LK2 wird das Fach erkannt, das mit dem Fachstatus 2PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter ```Schüler > Zeugnis > Fächer``` <br/>  und diese Daten dann per Synchronisation in das Modul Abitur übertragen.<br/>  Das Feld Fachstatus wird beim Import des Katalogs "00_Fachstati.keys" befüllt. |
|**Statistikfeld**| **GKS**                                      |
| Datenfeld     | MAGELLAN:<br/>Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus] |
| Beschreibung  | Nur ABS!<br/>  Als GKS wird das Fach erkannt, das mit dem Fachstatus 3PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter ```Schüler > Zeugnis > Fächer``` <br/>  und diese Daten dann per Synchronisation in das Modul Abitur übertragen.<br/>  Das Feld Fachstatus wird beim Import des Katalogs "00_Fachstati.keys" befüllt. |
|**Statistikfeld**| **GKM**    |
| Datenfeld     | MAGELLAN:<br/>Abitur > Qualifikation > Spalte "Fachstatus" [Fachstatus] |
| Beschreibung  | Nur ABS!<br/>  Als GKM wird das Fach erkannt, das mit dem Fachstatus 4PF markiert wurde. Sie können das Fach hier mit dme Fachstatus markieren oder unter ```Schüler > Zeugnis > Fächer``` <br/>  und diese Daten dann per Synchronisation in das Modul Abitur übertragen.<br/>  Das Feld Fachstatus wird beim Import des Katalogs "00_Fachstati.keys" befüllt. |
|**Statistikfeld**| **Abiturnote**                               |
| Datenfeld     | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussnote |
| Beschreibung  | Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist. |
|**Statistikfeld**| **Staatsang**                                |
| Datenfeld     | MAGELLAN:<br/>Schüler > Daten 2 > Staatsangeh. 1[Staatsangehörigkeiten] |
| Beschreibung  | Wählen Sie die Staatsangehörigkeit des Schülers aus. |
|**Statistikfeld**| **Aussiedler**                               |
| Datenfeld     | MAGELLAN:<br/>Schüler > Daten 2 > Aussiedler |
| Beschreibung  | Setzen Sie entsprechend den Haken, um den Schüler als Aussiedler zu markieren. |
|**Statistikfeld**| **Pruefstatus**                              |
| Datenfeld     | MAGELLAN:<br/>Schüler > Laufbahn > Allgemein > Versetzungsart[Versetzungsarten]<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart[Abschlussarten]<br/>Abitur > Prüfung > Status |
| Beschreibung  | Der Prüfstatus gibt an, ob ein Schüler das Abitur bestanden hat, bzw. zugelassen wurde oder vorher freiwillig zurückgetreten ist. <br/>  Der freiwillige Rücktritt wird als Versetzungsart angegeben. Die anderen Werte werden entweder über den Status des Abiturmoduls ermittelt, <br/>  wobei der Status „Gesamtqualifikation nicht erreicht“ als „Nicht zum Abitur zugelassen“ interpretiert wird. <br/>  Wenn Sie das Abiturmodul nicht einsetzen, können Sie die Werte über die Abschlussart des 1. Abschlusses angeben. |

