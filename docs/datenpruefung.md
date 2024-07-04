# Datenprüfung

Vor dem Erstellen der eigentlichen Statistikdateien sollten Sie eine Prüfung der Daten in Magellan vornehmen. Für einige Statistiken werden Prüfungen beim Erstellen der Statistik ausgegeben. Ob dies für Ihre Statistik zutrifft, entnehmen Sie bitte der jeweiligen Statistikdokumentation.

Zum Prüfen der Statistikdateien gehen Sie bitte wie folgt vor:

1. Starten Sie Magellan.
2. Klicken Sie im Menü `Extras` auf `Exporte > Export`.
3. Wählen Sie Ihr dann die Exportschnittstelle aus.
4. Wenn Ihre Statistik eine Zeitraum-Auswahl vorsieht, wählen Sie unter `Statistikzeiträume auswählen` entsprechend Ihrer Dokumentation die entsprechenden Zeiträume (in vielen Fällen den aktuellen Zeitraum und die beiden vorangegangenen Halbjahre) aus.
5. Wenn Ihre Statistik Stundenplandaten benötigt, geben Sie für die `daVinci Exportdatei` bitte den Pfad zu der Textdatei ein, die Sie in DaVinci über den Punkt `Plan > Importieren und Exportieren > Export > Statistikdaten exportieren` erzeugt haben und klicken dann auf `Weiter`.
6. Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf `Weiter`.
7. Starten Sie den Statistikexport. Mögliche vorhandene Fehler werden Ihnen nun ausgegeben.

## Ergebnis der Datenprüfung auswerten

Die Ergebnisse der Datenprüfung werden unter Hinweise aufgelistet. Sind dort keine Hinweise enthalten, sind die Daten für die Abgabe an das Statistikamt was unserere Prüfungen betrifft korrekt eingegeben oder es werden keine statistisch relevanten Daten erkannt (eventuell fehlt die Eingabe des Statistikkürzels der Klasse?).

!!! info "Hinweis"
    Die Hinweise werden unterschieden nach Art der Datei, dem betroffenen Datensatz, Kontroll-Nr der Plausibilität und dem eigentlichen Meldungstext. Sie können die Hinweise gruppieren und/oder Filtern und über die Schältfläche `Export nach Excel` nach Excel exportieren.

Sie müssen nun die Meldungen in Magellan bzw. DaVinci bearbeiten und dann erneut eine Datenprüfung durchführen.

!!! info "Hinweis"

    Viele in der Prüfung abgefragte Werte werden nicht in den Statistikdateien ausgegeben, dienen aber als Voraussetzung für die Plausibilitätsprüfungen. Beispiel: Zur Prüfung von korrekten Fremdsprachen bei Allgemeinbildenden Schulen muss die Schulart angegeben sein. Wurde diese nicht oder fehlerhaft angegeben, gibt die Prüfung eine Fehlermeldung aufgrund dieser Bedingung aus.
