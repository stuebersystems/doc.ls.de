# Import von Daten aus MVP-SIP nach MAGELLAN

!!! warning "Wichtig"

    Dieser Teil der Dokumentation ist derzeit in Bearbeitung. Die Inhalte sind teilweise Platzhalter.


1. [Beachten Sie bitte die Mindestvoraussetzungen für den Import](einstieg.md/#voraussetzungen-fur-den-import)
2. Lesen Sie in diesem Abschnitt wie Sie mit Meldungen durch den Import umgehen.
3. Lesen Sie im Abschnitt [Schnittstellendatei nach MAGELLAN importieren](#schnittstellendatei-nach-magellan-importieren), wie Sie den Import durchführen.

## Prüfung von ...

Platzhalter

## Mit Meldungen des Imports umgehen

Platzhalter

## Schnittstellendatei nach MAGELLAN importieren

Sie importieren die im [Einstieg](einstieg.md#einfuhrung) erwähnte XML-Datei aus MVP-SIP. Das Ergebnis des Imports sind Einträge im Feld `GUIDExtern` in der Ansicht "Schüler".

## Import ausführen

Für den Import der Schnittstellendatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Extras` auf und wählen den Unterpunkt `Import`.
![Daten nach MAGELLAN importieren über `Schüler > Importe > Import...`](/assets/images/sachsen/import.saxsvs01.png)<br><br>

Es startet der Importassistent, bitte wählen Sie die Schnittstelle `MVP-SIP` aus.
![Wählen Sie die Schnittstelle aus!](/assets/images/sachsen/import.saxsvs02.png)<br><br>

Fügen Sie über das Plus die zu importierende SIP.XML hinzu.
![Wählen Sie die Schnittstelledatei aus!](/assets/images/sachsen/import.saxsvs03.png)<br><br>

Im unteren Bereich geben Sie an, ob Sie die zu importierende Datei vorab prüfen möchten, die Prüfung und Import zusammen durchführen, oder ohne Prüfung den Import ausführen möchten.
![Wählen Sie die Art des Imports aus!](/assets/images/sachsen/import.saxsvs04.png)<br><br>

Starten Sie den Import oder die Prüfung per Klick auf `Fertigstellen`!
![Starten Sie den Import!](/assets/images/sachsen/import.saxsvs05.png)

## Mögliche Probleme

Sollte Ihnen in der Auswahl im Exportassistenten nicht der Punkt `SIP` gezeigt werden, ist vermutlich im Willkommensassistenten nicht die Bundeslandauswahl "Mecklenburg-Vorpommern" getroffen worden.

### So geht's

1. Schließen Sie bitte MAGELLAN und starten Sie bitte den MAGELLAN ADMINISTRATOR und wechseln in den Menüpunkt `Datenbankverbindungen`.
2. Klicken Sie doppelt auf Ihre Verbindungszeile, es öffnet sich das Fenster `Verbindungsdetails`.
3. Rufen Sie den Punkt `Datenbank` auf und tragen im Feld `Region` "Sachsen" ein.<br>Im Anschluss starten Sie MAGELLAN wieder, unter `Extras > Importe > Import...` sollte jetzt auch die Auswahl `SIP` zur Verfügung stehen!
