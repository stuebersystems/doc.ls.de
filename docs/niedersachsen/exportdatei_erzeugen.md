# Schnittstellendatei aus MAGELLAN erzeugen

Das Ergebnis des Exports sind die bereits im [Einstieg](einstieg.md#einfuhrung) erwähnten Textdateien.

## Statistikdaten erstellen

Für die Erstellung der Schnittstellendatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Extras` auf und wählen den Unterpunkt `Export`.<br><br>
![Daten aus MAGELLAN exportieren über `Schüler > Exporte > Export...`](/assets/images/export/export01.png)

Es startet der Exportassistent, bitte wählen Sie die Schnittstelle `SAX-SVS (BBS)`. Klicken Sie auf `Weiter`!<br><br>
![Wählen Sie die Schnittstelle aus!](/assets/images/export/export02.niestat.png)

Auf der Folgekarte wählen Sie einen Speicherort (Exportordner) und klicken auf `Weiter`!<br><br>
![Bitte wählen Sie einen Speicherort!](/assets/images/export/export04.png)

Starten Sie die Erstellung der Exportdatei oder die Prüfung per Klick auf `Fertigstellen`!<br><br>
![Starten Sie die Erstellung!](/assets/images/export/export05.png)

## Mögliche Probleme

### In der Auswahl des Exportassistenten wird der Punkt `SAXSVS` nicht gezeigt

Vermutlich wurde bei der Einrichtung von MAGELLAN im Willkommensassistenten bei der Bundeslandauswahl nicht "Niedersachsen" ausgewählt.<br>

#### So geht's

1. Schließen Sie bitte MAGELLAN und starten Sie bitte den MAGELLAN ADMINISTRATOR und wechseln in den Menüpunkt `Datenbankverbindungen`.
2. Klicken Sie doppelt auf Ihre Verbindungszeile, es öffnet sich das Fenster `Verbindungsdetails`.
3. Rufen Sie den Punkt `Datenbank` auf und tragen im Feld `Region` "Sachsen" ein.<br>Im Anschluss starten Sie MAGELLAN wieder, unter `Extras > Export > Export...` sollte jetzt auch die Auswahl `izn-Stabil` zur Verfügung stehen!

### Bei der Auswahl von `SAXSVS` im Exportassistenten erscheint folgende Meldung

```txt
`Das Schuljahr konnte nicht ermittelt werden.`
`Achten Sie bitte darauf, dass der Zeitraum passend zum heutigen Datum in MAGELLAN existiert.`

Beim Klick auf `Weiter` im Exportassistenten erscheint daraufhin die Meldung `Geben Sie bitte mind. einen Zeitraum an`
```

Das Schuljahr konnte nicht ermittelt werden. Dies geschieht, wenn Sie zum aktuellen Datum keinen passenden Zeitraum in MAGELLAN angelegt haben.

#### So geht's

1. Öffnen Sie das Dialogfenster der Verzeichnisse unter `Extras > Schlüsselverzeichnisse` und wechseln Sie in das Verzeichnis `Zeiträume`.
2. Legen Sie dort über den Punkt `Schuljahre anlegen...` ein neues Schuljahr an, aber mindestens soviele, dass Sie das passende Schulhalbjahr zum Datum erhalten.
3. Im neuen/In den neuen Schulhalbjahr(en) existieren noch keine Klassen- und Schülerdaten. Diese müssen Sie erst über den gewohnten Weg in MAGELLAN `Fortschreiben` und/oder `Versetzen` bevor Sie den Export erneut ausführen können.
