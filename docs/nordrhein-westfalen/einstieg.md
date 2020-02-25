# Nordrhein-Westfalen - Einstieg in die die Landesstatistik

Das Ministerium für Schule und Weiterbildung des Landes Nordrhein-Westfalen fordert mehrmals im Jahr eine statistische Erhebung von den Schulen.
Zur Erstellung der Statistik wird das Programm ASDPC des Schulministerium benötigt. ASDPC verfügt über eine Importschnittstelle zum Einlesen von Daten aus Schulverwaltungsprogrammen.
Mit dem Landesstatistik-Modul können Sie die benötigten Schnittstellendateien direkt aus MAGELLAN und DAVINCI erzeugen.

!!! info "Hinweis"

    Eine DAVINCI-Lizenz wird nur für die EXTERN.DAT und die LEHRER.TXT benötigt, da diese Stundenplandaten enthalten. Jede Datei kann einzeln erzeugt werden, somit benötigen Sie z.B. kein DAVINCI wenn Sie lediglich die SIM.TXT oder die ABI.TXT erzeugen möchten.

## Einführung

Die Statistikdateien werden anhand der erfassten Daten in MAGELLAN und DAVINCI erstellt. Hier erhalten Sie eine Übersicht über die Schnittstellendateien:

Dateiname  | Abkürzung | Kapitel                           | Inhalt
---------- | --------- | --------------------------------- | ------
SIM.TXT    | SIM       | [SIM.TXT](schuelerdaten.md)       | Nur MAGELLAN-Daten
LEHRER.TXT | LEHRER    | [LEHRER.TXT](lehrerdaten.md)      | MAGELLAN-Daten und aus DAVINCI der „Allgemeine Statistikexport“
ABI.TXT    | ABI       | [ABI.TXT](abiturdaten.md)         | Nur MAGELLAN-Daten
EXTERN.DAT | EXTERN    | [EXTERN.DAT](stundenplandaten.md) | Nur DAVINCI-Daten aus dem Export für „ASDPC/EXTERN.DAT“

!!! warning "Wichtig"

    Wir erstellen die Statistikdateien entsprechend der Schnittstellenbeschreibungen des statistischen Landesamtes. 
    In einigen Fällen (Beispiel: SIM.txt) spielen wir zusätzliche Felder aus, die die Zuordnung der Zeilen zu Datensätzen in Ihrem Datenbestand ermöglichen. Damit können wir bei Problemen besser die Ursache im Datenstand finden. Diese zusätzlichen Felder sind in Absprache mit dem statistischen Landesamt integriert und werden von ASDPC beim Import ignoriert.

### Zeitraumbedingte Daten

Viele Schüler- und Klassendaten in MAGELLAN werden zeitraumbezogen pro Schulhalbjahr abgelegt. Je nach Statistkdatei und Datensatz müssen die Daten entsprechend der Vorgaben aus der Schnittstelle aus den unterschiedlichen Halbjahren ausgelesen und ausgewertet werden.

Statistikdatei | Ausgelesene Halbjahre
-------------- | ---------------------
SIM            | 1. HJ. aktuelles Schuljahr, 2. HJ. vorangegangenes Schuljahr, 1. HJ. vorangegangenes Schuljahr
LEHRER         | -
ABI            | 2. HJ. vorangegangenes Schuljahr
EXTERN         | -

Welche Daten wie ausgewertet werden und unter welchen Umständen Daten in den Export aufgenommen werden, entnehmen Sie den einzelnen Kapiteln zu den Statistikdateien.

!!! warning "Wichtig"

    Sie müssen immer alle drei Zeiträume im Assistenten angeben, ungeachtet dessen welche Datei Sie zum Export auswählen. Der Exportmechanismus entscheidet von sich aus, welchen Zeitraum zu nehmen.

## Notwendige Schritte

1. Schritt: [Statistikschlüssel aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Dateneingabe
3. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
4. Schritt: [Statistikdateien erzeugen](../statistikdaten.erstellen.md)

Verlinkte Schritte werden in den jeweiligen Kapiteln beschrieben. Klicken Sie dazu auf den Link. Alle anderen Schritte werden nachfolgend ausführlich erklärt.

## 2. Dateneingabe

Sie erhalten eine Übersicht der Felder in den Statistikdateien und wie diese in MAGELLAN bzw. DAVINCI einzupflegen sind.
Jede Statistikdatei wird in einem einzelnen Kapitel behandelt, die Links zu den Kapiteln finden Sie in der obersten Tabelle in der Spalte "Kapitel".

### Voraussetzungen für alle Statistikdaten

Damit die Statistikdateien korrekt erstellt und gefüllt werden können, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden. Ist einer der Felder nicht gefüllt erhalten Sie entsprechende Meldungen und der Export wird nicht durchgeführt.

Statistikfeld | Statistikdatei | Datenfeld in MAGELLAN/DAVINCI | Beschreibung
------------- | -------------- | ----------------------------- | ------------
--            | ALLE           | MAGELLAN: `Mandanten > Daten 2 > Schulformen` | Hauptschulform Ihrer Schule.<br/>Bei Berufskollegs = BK.<br/>**Wichtig:**<br/>MAGELLAN sortiert die Schulformen. Die Schulform sollte als erste erscheinen. Um sicher zu gehen, sollten Sie zuerst alle Schulformen entfernen und dann die Hauptschulform als Erstes eintragen.
--            | ALLE           | MAGELLAN: `Mandanten > Daten 1 > Schulnummer` | Die Schulnummer Ihrer Schule.

## 4. Statistikdaten erstellen

!!! info "Hinweis"

 Bitte achten Sie darauf, dass Sie für das Erstellen der Statistik in MAGELLAN den aktuellsten Statistikzeitraum geöffnet haben.

Die Statistikdaten erstellen Sie wie folgt:

1. Klicken Sie im Menü Extras auf `Exporte > Export`.
2. Wählen Sie dann den Aufruf `Export...` aus.
3. Wenn Sie im MAGELLAN Adminstrator Ihr Bundesland `Nordrhein-Westfalen` hinterlegt haben, steht Ihnen bei der Auswahl der Exportsschnittstelle `Landesstatistik Nordrhein-Westfalen` zur Auswahl.
4. Unter Exportdateien wählen Sie die zu erzeugenden Exportdateien aus.
5. Unter Export-Zeiträume stellen Sie den aktuellen Zeitraum ein und die beiden vorangegangenen Halbjahre.
6. Wenn Sie die Lehrer.txt für den Export ausgewählt haben, müssen Sie hier Ihre DAVINCI Exportdatei hinterlegen.
7. Klicken Sie auf `Weiter`

### Besonderheiten

#### 2019/2020

`Schüler > Statistik > Merkmal S10` -  Wählen Sie im Schülermerkmal S10 ***Kein Export nach ASDPC*** aus, um Schüler explizit aus der Statistik zu nehmen.
