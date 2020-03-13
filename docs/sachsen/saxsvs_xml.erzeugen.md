# Schnittstellendatei aus MAGELLAN erzeugen

Das Ergebnis des Eports ist die bereits im [Einstieg](einstieg.md#einfuhrung) erwähnte XML-Datei.

## Statistikdaten erstellen

Für die Erstellung der Schnittstellendatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Extras` auf und wählen den Unterpunkt `Export`.<br><br>
![Daten aus MAGELLAN exportieren über `Schüler > Exporte > Export...`](/assets/images/sachsen/export.saxsvs01.png)

Es startet der Exportassistent, bitte wählen Sie die Schnittstelle `SAX-SVS (BBS)` und fügen über das Plus den gewünschten Exportzeitraum hinzu. Klicken Sie auf `Weiter`!<br><br>
![Wählen Sie die Schnittstelle und den Zeitraum aus!](/assets/images/sachsen/export.saxsvs02.png)

Auf der Folgekarte wählen Sie einen Speicherort (Exportordner) und klicken auf `Weiter`!<br><br>
![Bitte wählen Sie einen Speicherort!](/assets/images/sachsen/export.saxsvs04.png)

Starten Sie die Erstellung der Exportdatei oder die Prüfung per Klick auf `Fertigstellen`!<br><br>
![Starten Sie die Erstellung!](/assets/images/sachsen/export.saxsvs05.png)

## Mögliche Probleme

Sollte Ihnen in der Auswahl im Exportassistenten nicht der Punkt `SAXSVS` gezeigt werden, ist vermutlich im Willkommensassistenten nicht die Bundeslandauswahl "Sachsen" getroffen worden.

### So geht's

1. Schließen Sie bitte MAGELLAN und starten Sie bitte den MAGELLAN ADMINISTRATOR und wechseln in den Menüpunkt `Datenbankverbindungen`.
2. Klicken Sie doppelt auf Ihre Verbindungszeile, es öffnet sich das Fenster `Verbindungsdetails`.
3. Rufen Sie den Punkt `Datenbank` auf und tragen im Feld `Region` "Sachsen" ein.<br>Im Anschluss starten Sie MAGELLAN wieder, unter `Extras > Export > Export...` sollte jetzt auch die Auswahl `SAXSVS` zur Verfügung stehen!
