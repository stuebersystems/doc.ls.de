# Nordrhein-Westfalen - Einstieg in die die Landesstatistik

Das Ministerium für Schule und Weiterbildung des Landes Nordrhein-Westfalen fordert mehrmals im Jahr eine statistische Erhebung von den Schulen.
Zur Erstellung der Statistik wird das Programm ASDPC des Schulministerium benötigt. ASDPC verfügt über eine Importschnittstelle zum Einlesen von Daten aus Schulverwaltungsprogrammen.
Mit dem Landesstatistik-Modul können Sie die benötigten Schnittstellendateien direkt aus MAGELLAN und DAVINCI erzeugen.

## Einführung

Die Statistikdateien werden anhand der erfassten Daten in MAGELLAN und DAVINCI erstellt. Hier erhalten Sie eine Übersicht über die Schnittstellendateien, und welche von MAGELLAN 7 unterstützt werden:

Dateiname  | Abkürzung | Kapitel                           | Inhalt
---------- | --------- | --------------------------------- | ------
SIM.TXT    | SIM       | [SIM.TXT](schuelerdaten.md)       | Nur MAGELLAN-Daten
LEHRER.TXT | LEHRER    | [LEHRER.TXT](lehrerdaten.md)      | MAGELLAN-Daten und aus DAVINCI der „Allgemeine Statistikexport“
ABI.TXT    | ABI       | [ABI.TXT](abiturdaten.md)         | Nur MAGELLAN-Daten
EXTERN.DAT | EXTERN    | [EXTERN.DAT](stundenplandaten.md) | Nur DAVINCI-Daten aus dem Export für „ASDPC/EXTERN.DAT“

### Zeitraumbedingte Daten

Viele Schüler- und Klassendaten in MAGELLAN werden zeitraumbezogen pro Schulhalbjahr abgelegt. Je nach Statistkdatei und Datensatz müssen die Daten entsprechend der Vorgaben aus der Schnittstelle aus den unterschiedlichen Halbjahren ausgelesen und ausgewertet werden.

Statistikdatei | Benötigte Halbjahre
-------------- | -------------------
SIM            | 1. HJ. aktuelles Schuljahr, 2. HJ. vorangegangenes Schuljahr, 1. HJ. vorangegangenes Schuljahr
LEHRER         | -
ABI            | 2. HJ. vorangegangenes Schuljahr
EXTERN         | -

Welche Daten wie ausgewertet werden und unter welchen Umständen Daten in den Export aufgenommen werden entnehmen Sie den einzelnen Kapiteln zu den Statistikdateien.

### DAVINCI-LIZENZ

Eine DAVINCI Lizenz wird nur für die EXTERN.DAT und die LEHRER.TXT benötigt, da diese Stundenplandaten enthalten. Jede Datei kann einzeln erzeugt werden, somit benötigen Sie z.B. kein DAVINCI wenn Sie lediglich die SIM.TXT oder die ABI.TXT erzeugen möchten.

## Notwendige Schritte

1. Schritt: [Statistikschlüssel aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Dateneingabe
3. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
4. Schritt: Statistikdateien erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

### Statistikschlüssel aktualisieren

Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](../schluesselverzeichnisse.md).

## Dateneingabe

Sie erhalten eine Übersicht der Felder in den Statistikdateien, sowie diese in MAGELLAN bzw. DAVINCI einzupflegen sind.
Die Dateneingaben zu den einzelnen Statistikdateien finden Sie in der obersten Tabelle in der Spalte "Kapitel".

### Voraussetzungen für alle Statistikdaten

Damit die Statistikdateien korrekt erstellt und gefüllt werden können, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden.

Statistikfeld | Statistikdatei | Datenfeld in MAGELLAN/DAVINCI | Beschreibung
------------- | -------------- | ----------------------------- | ------------
--            | ALLE           | MAGELLAN:<br>`Mandanten > Daten 2 > Schulformen` | Hauptschulform Ihrer Schule.<br/>Bei Berufskollegs = BK.<br/>Wichtig:<br/>MAGELLAN sortiert die Schulformen. Die Schulform sollte als erste erscheinen. Um sicher zu gehen, sollten Sie zuerst alle Schulformen entfernen und dann die Hauptschulform als Erstes eintragen.

### Besonderheiten

#### 2019/2020

Aktuell keine Besonderheiten.
